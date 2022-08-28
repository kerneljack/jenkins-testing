pipeline {
    agent {
        kubernetes {
            label 'docker-in-docker'
            yaml """
        apiVersion: v1
        kind: Pod
        spec:
            containers:
            - name: docker-dind
              image: docker:dind
              securityContext:
                privileged: true
              env:
              - name: DOCKER_TLS_CERTDIR
                value: ""
        """
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'ls -l /home/jenkins/agent'
                // sh 'docker --version'
                sh 'hostname'
                sh 'python --version'
            }
        }
    }
}
