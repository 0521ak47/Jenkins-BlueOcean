pipeline {
  agent {
    node {
      label 'salve'
    }
    
  }
  stages {
    stage('checkout') {
      agent any
      steps {
        git(url: 'ssh://git@pangu.bldz.com:10022/core-service/commodity-soa.git', credentialsId: 'gitlab', branch: 'master', poll: true, changelog: true)
      }
    }
  }
  environment {
    gitbranch = 'release/pre'
  }
}