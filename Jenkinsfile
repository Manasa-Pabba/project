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
        sh 'docker-compose up -d'
        
      }
    }
        stage('Run tests against the container') {
      steps {
        sh 'curl http://localhost:8501'
      }
    }
    }
}
