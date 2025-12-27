pipeline {
    agent any

    environment {
        DOCKER_CREDS = credentials('docker-hub')
    }

    stages {
        stage('Login') {
            steps {
                sh '''
                  echo "$DOCKER_CREDS_USR"
                  echo "$DOCKER_CREDS_PSW"
                '''
            }
        }
    }
}
