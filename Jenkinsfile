pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test2') {
          steps {
            echo 'RunningTest2'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running Test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployment Completed'
      }
    }

  }
}