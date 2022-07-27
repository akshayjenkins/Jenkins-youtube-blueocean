pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('unittest') {
      parallel {
        stage('unittest') {
          steps {
            echo 'unittest is running'
          }
        }

        stage('regressiontest') {
          steps {
            echo 'regression test is running'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sleep 15
      }
    }

  }
}