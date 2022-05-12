pipeline {
    agent any
    
    

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
        
    }
}
