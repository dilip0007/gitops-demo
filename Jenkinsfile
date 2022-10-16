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
        stage('Cleanup Workspace'){
            steps {
                script {
                    cleanWs()
                }
            }
        }
    
        
        
    }
}
