pipeline {
    agent { label 'mydockerlabel' }
    stages {
        stage('build') {
            agent {
                docker {
                    // Set both label and image
                    label 'mydockerlabel'
                    image 'python:3.10.1-alpine'
                }
            }
            steps {
                sh 'python --version'
            }
        }
    }
}
