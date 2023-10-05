pipeline {
    agent any
   environment {
registry = "ujjwal2692/jenkins_build"
registryCredential = 'Dockerhub-id'
dockerImage = ''
   }
    stages {
        stage('Build') {
            steps {
               
                bat '''
                docker.withRegistry( '', registryCredential )
                docker build -t cicd_roberta:0.0.1 .
                docker tag cicd_roberta:0.0.1 ujjwal2692/jenkins_build:0.0.1
                docker push ujjwal2692/jenkins_build:0.0.1

                '''
            }
        }
        
    }
}