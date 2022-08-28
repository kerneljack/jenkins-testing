pipeline {
    agent {
        kubernetes {
            label 'jenkins-slave'
            container ('dind')
        }
    }
    stages {
        stage('build') {
            steps {
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
