pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
      }
    }

    stage('Test Browser') {
      parallel {
        stage('Test Edge') {
          steps {
            sh 'echo \'Testing Edge\''
          }
        }

        stage('Chrome') {
          steps {
            sh 'echo \'Testing Chrome\''
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