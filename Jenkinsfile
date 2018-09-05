pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello Build'
        sleep 10
        echo 'Goodbye Build'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Hello Test'
            sleep 10
            echo 'Goodbye Test'
          }
        }
        stage('Test-P') {
          steps {
            echo 'Hello Test-P'
            sleep 5
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Hello Deploy'
        sleep 10
        echo 'Goodbye Deploy'
      }
    }
  }
}