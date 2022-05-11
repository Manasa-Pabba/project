pipeline {
    agent any
    
    

    stages {
        stage('Prune Docker data') {
      steps {
        bat 'docker system prune -a --volumes -f'
      }
    }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
