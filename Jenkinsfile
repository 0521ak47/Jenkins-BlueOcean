pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
ls'''
      }
    }
  }
  environment {
    gitbranch = 'release/pre'
  }
}