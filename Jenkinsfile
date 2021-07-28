pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'compile maven app'
            sh 'sh \'mvn compile\''
          }
        }

        stage('test') {
          steps {
            echo 'test maven app'
            sh 'sh \'mvn clean test\''
          }
        }

        stage('package') {
          steps {
            echo 'package maven app'
            sh 'sh \'mvn package -DskipTests\''
          }
        }

      }
    }

  }
}