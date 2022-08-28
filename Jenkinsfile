pipeline {
    agent {
        kubernetes {
            label 'docker-in-docker'
        }
    }
    stages {
        stage('build') {
            steps {
                container('docker-dind') {
                    // sh 'sleep 300'
                    sh 'docker --version'
                    sh 'pwd'
                    sh 'ls -la'
                    sh 'hostname'
                    // sh 'python --version'
                }
            }
        }
    }
}
