pipeline {
    agent {
        docker { image 'node:latest' } }
            stages {
                stage('build') {
                    steps {
                        sh 'npm --version'
            }
        }
                stage('clone') {
                    steps {
                        sh 'git clone git@github.com:ibokalo/node.git'
                    }
    }
}
}