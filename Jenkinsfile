pipeline {
  agent any
  stages {
    stage('unit tests') {
      steps {
        sh 'echo \'unit tests...\''
      }
    }
    stage('integration') {
      parallel {
        stage('integration') {
          steps {
            sh 'echo \'integration\''
          }
        }
        stage('ui') {
          steps {
            sh 'echo \'Now UI tests are passing.\''
          }
        }
      }
    }
    stage('deploy') {
      steps {
        sh 'echo \'deploy\''
      }
    }
  }
}