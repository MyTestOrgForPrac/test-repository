pipeline {
    agent any

    environment {
        DOCKER_CREDS = credentials('docker-hub')
    }

    stages {
        stage('Login') {
            steps {
                sh '''
                  echo "$DOCKER_CREDS_PSW" | docker login \
                    -u "$DOCKER_CREDS_USR" \
                    --password-stdin            
                  docker pull maheswarsarma/whale-demo:latest
                  docker tag  maheswarsarma/whale-demo  maheswarsarma/whale-demo2
                  docker push  maheswarsarma/whale-demo2
                  
                '''
            }
        }
    }
}
