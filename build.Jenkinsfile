pipeline {
    agent any
     
    stages {
        stage('Build Docker Image') {
            steps {
               
                bat ''' 
                echo "first build completed"
                docker build -t ujjwal2692/firstimage:1.0 .
                '''
            }
        }
        stage('pushing to dockerhub'){
            steps{
              withCredentials([string(credentialsId: 'dockerpwd', variable: 'dockerpwd')]) {
                bat '''
                docker login -u ujjwal2692 -p ${dockerpwd}
                '''
              }
                bat 'docker push ujjwal2692/firstimage:1.0'
            }

        }
    }
}