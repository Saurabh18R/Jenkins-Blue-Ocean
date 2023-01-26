pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'teststep'
          }
        }

        stage('test parallel') {
          steps {
            echo 'Test Parallel'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployed'
        sleep 10
      }
    }

  }
}