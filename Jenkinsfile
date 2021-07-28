pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'compile maven app'
          }
        }

        stage('test') {
          steps {
            echo 'test maven app'
          }
        }

        stage('package') {
          steps {
            echo 'package maven app'
          }
        }

      }
    }

  }
}