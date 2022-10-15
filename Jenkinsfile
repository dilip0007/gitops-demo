pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh "echo ${BUILD_NUMBER}" 
                
            }
        }
    }
    stage('Cleanup Workspace'){
            steps {
                script {
                    cleanWs()
                }
            }
        }
}
