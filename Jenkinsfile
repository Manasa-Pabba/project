pipeline {
  agent any
  stages {
    stage("verify tooling") {
      steps {
        sh '''
          docker version
          docker info
          dockercompose version 
        '''
      }
    }
  }   
}