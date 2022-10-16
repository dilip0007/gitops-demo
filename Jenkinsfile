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
        stage('Updating Kubernetes deployment file'){
            steps {
                sh "cd /Users/dilipnigam/.jenkins/workspace/pipeline && ./script.sh"
                
               
            }
        }
        stage('Build Docker Image'){
            steps {
                script{
                    docker_image = docker.build "${IMAGE_NAME}"
                }
            }
        }
        
    
        
        
    }
}
