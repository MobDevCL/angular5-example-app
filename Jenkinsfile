node {
    stage 'Checkout'
    checkout scm

    stage 'Dependencies'
    sh "npm install"

    stage 'Test'
    sh "npm run test"

    stage 'Build'
    sh "npm run build"

    stage 'Package'
    sh "zip -r dist.zip dist/"

    stage 'Release'
    archiveArtifacts artifacts: '**/*.zip', fingerprint: true
}