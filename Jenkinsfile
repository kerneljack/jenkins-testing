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
                container('docker-dind') {
                    // sh 'sleep 300'
                    sh 'docker --version'
                    sh 'hostname'
                    sh 'python --version'
                }
            }
        }
    }
}
