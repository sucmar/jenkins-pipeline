pipeline {
    agent { label 'Node1'}
    environment {
        SERVICE_NAME="library-backend"
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh "cd /home/elpepe/docker/python/library ; docker build -t 192.168.1.64:8082/${SERVICE_NAME}:${BUILD_NUMBER} . ; docker push 192.168.1.64:8082/${SERVICE_NAME}:${BUILD_NUMBER}"
                }
            }
        }
    }
}
