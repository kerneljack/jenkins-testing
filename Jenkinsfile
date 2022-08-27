pipeline {
    agent { label 'docker-slave' }
    stages {
        stage('build') {
            agent {
                docker {
                    // Set both label and image
                    label 'docker-slave'
                    image 'python:3.10.1-alpine'
                }
            }
            steps {
                sh 'python --version'
            }
        }
    }
}
