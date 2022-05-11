pipeline {
    agent any
    
    

    stages {
        stage('Prune Docker data') {
      steps {
        sh -c 'docker system prune -a --volumes -f'
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
