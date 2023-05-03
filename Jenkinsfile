pipeline {
  agent any
  stages {
    stage('BUILD') {
      steps {
        echo 'This is my Build'
      }
    }

    stage('TEST') {
      parallel {
        stage('TEST') {
          steps {
            echo 'This is my test '
          }
        }

        stage('UNIT-TEST') {
          steps {
            echo 'This is Unit-testing  '
            sh 'mvn test'
          }
        }

      }
    }

    stage('DEPLOY') {
      steps {
        echo 'this is my deploy'
      }
    }

  }
}