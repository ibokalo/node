pipeline {
    agent {
        docker { image 'node:latest' } }
            stages {
                stage('build') {
                    steps {
                        sh 'npm --version'
            }
            }
                stage ('deploy') {
                    steps {
                        sh 'ssh ubuntu@172.17.0.1 & rm -rf /home/ubuntu/deploy/temp'
            }
}
}
}