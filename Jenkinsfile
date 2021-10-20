pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
        retry(count: 3) {
          sh 'wwa'
        }

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
        input(message: 'Are you sure to deploy ?', ok: 'Yes, I am sure')
        echo 'Deployment Completed'
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'New Build Completed'
      }
    }

  }
}