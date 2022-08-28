pipeline {
    agent { label 'jenkins-slave' }
    stages {
        stage('build') {
            agent {
                docker {
                    // Set both label and image
                    label 'jenkins-slave'
                    image 'python:3.10.1-alpine'
                }
            }
            steps {
                sh 'python --version'
            }
        }
    }
}
