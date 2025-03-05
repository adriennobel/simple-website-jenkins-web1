pipeline {
  agent any

  stages {
    stage('CLONE') {
      steps {
        sh 'echo "clone"'
        sh 'uname -r'
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
