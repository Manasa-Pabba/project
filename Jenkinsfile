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
                bat "echo ${env.DOCKHUB_CREDS_PSW} | docker login -u ${env.DOCKHUB_CREDS_USR} --password-stdin"
            }
        }
        
        stage('push'){
            steps{
                bat 'docker tag app manasa6900/app_repo:latest'
                bat 'docker push manasa6900/app_repo:latest'
            }
        }
                
                
            
        
        
    }
}
