pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
      }
    }

    stage('Test') {
      parallel {
        stage('Test Edge') {
          steps {
            sh 'echo \'Testing Edge\''
          }
        }

        stage('Chrome') {
          steps {
            sh 'echo \'Testing Chrome\'; exit 1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }

  }
}
