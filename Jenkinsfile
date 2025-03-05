pipeline {
  agent any

  stages {
    stage('CODE SCAN') {
      steps {
        sh 'trivy fs . -o code-scam-resul.html'
      }
    }
    stage('DOCKER IMAGE BUILD') {
      steps {
        sh 'docker -v'
      }
    }
    stage('PUSH IMAGE') {
      steps {
        sh 'docker ps'
      }
    }
  }
}
