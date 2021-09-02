pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        echo 'this is checkout phase'
        sleep 10
        sh 'echo "version ${version}"'
      }
    }

  }
  environment {
    version = '1.0'
  }
}