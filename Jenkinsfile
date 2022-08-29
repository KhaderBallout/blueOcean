pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed from BlueOcean'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sleep 3
          }
        }

        stage('Test1') {
          steps {
            echo 'test completed '
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        sh '''echo "hello world"

pwd'''
      }
    }

  }
}