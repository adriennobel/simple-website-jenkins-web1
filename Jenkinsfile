pipeline {
  agent any

  stages {
    stage('CODE SCAN') {
      steps {
        sh 'trivy --version'
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
