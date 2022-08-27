pipeline {
    agent { label 'mydocker' }
    stages {
        stage('build') {
            agent {
                docker {
                    // Set both label and image
                    label 'mydocker'
                    image 'python:3.10.1-alpine'
                }
            }
            steps {
                sh 'python --version'
            }
        }
    }
}
