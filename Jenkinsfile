pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('stage1') {
          steps {
            bat(script: 'echo "Step 1"', returnStdout: true)
          }
        }
        stage('step2') {
          steps {
            powershell(script: 'get-process', returnStatus: true, returnStdout: true)
          }
        }
      }
    }
    stage('stage3') {
      steps {
        echo 'stage 3 '
      }
    }
  }
  environment {
    envvar = 'testenvvarvalue'
  }
}