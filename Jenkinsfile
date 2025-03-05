pipeline {
  agent any

  stages {
    stage('CLONE') {
      steps {
        sh 'echo "clone"'
      }
    }
    stage('TEST') {
      steps {
        sh 'echo "test"'
      }
    }
    stage('CREATE FILE') {
      steps {
        sh 'touch text-$BUILD_ID'
      }
    }
  }
}
