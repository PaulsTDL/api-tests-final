pipeline {
    agent any
    triggers {
        pollSCM('*/1 * * * *')
    }
    stages {
        stage('build-docker-image') {
            steps {
                echo "Building docker image"
                sh "docker build -t pgreinhards/api-tests:latest ."
                echo "Pushing docker image"
                sh "docker push pgreinhards/api-tests:latest"
            }
        }
    }
}