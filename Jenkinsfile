pipeline {
    agent any
    environment {
        DOCKERHUB_USERNAME = "dilipnigam007"
        APP_NAME = "gitops-demo"
        IMAGE_TAG = "${BUILD_NUMBER}"
        IMAGE_NAME = "${DOCKERHUB_USERNAME}" + "/" + "${APP_NAME}"
        REGISTRY_CREDS = 'dockerhub'
        }

    stages {
        stage('Build') {
            steps {
                sh "echo ${BUILD_NUMBER}" 
                
            }
        }
    
        stage('Cleanup Workspace'){
            steps {
                script {
                    cleanWs()
                }
            }
        }
        



        stage('Build Docker Image'){
            steps {
                
                sh "docker build -t ${IMAGE_NAME}:latest ."
                sh 'pwd'
                    
                
            }
        }
    }
}
