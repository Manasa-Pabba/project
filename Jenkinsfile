pipeline {
    agent any
    
    environment{
        DOCKHUB_CREDS = credentials('dockerhub-manasa')
    }

    stages {
        stage('Start container') {
            steps {
                bat 'docker-compose up -d --no-color --wait'
                bat 'docker ps'
            }
        }
        
        stage('Run tests against the container') {
            steps {
                bat 'curl http://localhost:8501'
            }
        }
        
        stage('login'){
            steps{
                bat 'echo $DOCKHUB_CREDS_PSW'
            }
        }
        
        stage('push'){
            steps{
                bat 'docker tag db manasa6900/postgres:latest'
                bat 'docker push manasa6900/postgres:latest'
            }
        }
                
                
            
        
        
    }
}
