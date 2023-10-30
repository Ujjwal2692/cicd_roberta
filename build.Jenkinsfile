pipeline {
    agent any
     
    stages {
        stage('Build Docker Image') {
            steps {
               
                bat ''' 
                echo "first build completed"
                docker build -t Ujjwal2692/firstimage:1.0 .
                '''
            }
        }
        
    }
}