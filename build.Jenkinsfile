pipeline {
    agent any
  environment {
    DOCKERHUB_CREDENTIALS = credentials('dockerhub')
  }
    stages {
        stage('Build') {
            steps {
               
                bat '''
                echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin
                docker build -t cicd_roberta:0.0.1 .
                docker tag cicd_roberta:0.0.1 ujjwal2692/jenkins_build:0.0.1
                docker push ujjwal2692/jenkins_build:0.0.1

                '''
            }
        }
        
    }
}