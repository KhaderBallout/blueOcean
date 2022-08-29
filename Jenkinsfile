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

    stage('Shell') {
      steps {
        sh '''echo "hello world"

pwd'''
      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to deploy ?', ok: 'Yes')
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'New Build completed successfully'
      }
    }

  }
}