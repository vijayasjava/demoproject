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

    stage('build') {
      agent any
      environment {
        reference = 'build phase'
      }
      steps {
        sh 'echo $PATH'
      }
    }

    stage('postbuild') {
      agent any
      environment {
        phase = 'post  build'
      }
      steps {
        script {
          def x = ["alpha", "beta", "capsule"]

          for(def t : x) {
            println(t)
          }
        }

      }
    }

  }
  environment {
    version = '1.0'
  }
}