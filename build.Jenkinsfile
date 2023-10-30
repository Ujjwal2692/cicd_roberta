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
        
    }
}