pipeline {
  agent any

  stages {
    stage('CODE SCAN') {
      steps {
        sh 'trivy fs . -o code-scam-resul.html'
        sh 'cat code-scam-resul.html'
      }
    }
    stage('DOCKER LOGIN') {
      steps {
        sh 'aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 747043738397.dkr.ecr.us-east-1.amazonaws.com'
      }
    }
    stage('DOCKER IMAGE BUILD') {
      steps {
        sh 'docker build -t simple-website-ci .'
        sh 'docker build -t simple-website-ci-version .'
      }
    }
    stage('DOCKER TAG') {
      steps {
        sh 'docker tag simple-website-ci:latest 747043738397.dkr.ecr.us-east-1.amazonaws.com/simple-website-ci:latest'
        sh 'docker tag simple-website-ci-version 747043738397.dkr.ecr.us-east-1.amazonaws.com/simple-website-ci:v1.$BUILD_NUMBER'
      }
    }
    stage('PUSH IMAGE') {
      steps {
        sh 'docker push 747043738397.dkr.ecr.us-east-1.amazonaws.com/simple-website-ci:latest'
        sh 'docker push 747043738397.dkr.ecr.us-east-1.amazonaws.com/simple-website-ci:v1.$BUILD_NUMBER'
      }
    }
  }
}
