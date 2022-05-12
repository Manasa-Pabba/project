pipeline {
    agent any
    
    

    stages {
             
        stage('pull postgres') {
      steps {
        bat 'docker pull manasa6900/stock_proj:1'
      }
    }
        stage('Start container') {
      steps {
        bat 'docker-compose up -d --no-color --wait'
        
      }
    }
        
    }
}
