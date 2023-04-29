pipeline {
    agent any
    environment {
        IMG_NAME = 'my-nx'
        DOCKER_REPO = 'joska99/labs-images'
    }
    stages {
        stage('build') {
            steps {
                script {
                        sh 'docker build -t ${IMG_NAME} .'
                        sh 'docker tag ${IMG_NAME} ${DOCKER_REPO}:${IMG_NAME}'
                }
            }
        }
        stage('push') {
            steps {
                script {
                    withCredentials([usernamePassword(credentialsId: 'DockerHub-LG', passwordVariable: 'PSWD', usernameVariable: 'LOGIN')]) {
                        sh 'docker login -u ${LOGIN} -p ${PSWD}'
                    }
                        sh 'docker push ${DOCKER_REPO}:${IMG_NAME}'
                }
            }
        }
    }
}

