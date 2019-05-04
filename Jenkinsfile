pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('Windows Batch 1') {
          steps {
            bat(script: 'echo "Step 1"')
          }
          stage('Windows Batch 2') {
          steps {
            bat(script: 'echo "Parallel Step 2"')
          }
        }
        stage('Powershell Stage- No Parallel') {
          steps {
            powershell(script: 'get-process')
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
