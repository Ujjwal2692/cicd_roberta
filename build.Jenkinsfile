pipeline {
    agent any
    environment {     
    DOCKERHUB_CREDENTIALS= credentials('Dockerhub-id')     
  }   
    stages {
        stage('Build') {
            steps {
               
                sh '''
                echo $DOCKERHUB_CREDENTIALS_PSW | sudo docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin
                docker build -t cicd_roberta:0.0.1 .
                docker tag cicd_roberta:0.0.1 ujjwal2692/jenkins_build:0.0.1
                docker push ujjwal2692/jenkins_build:0.0.1

                '''
            }
        }
        
    }
}