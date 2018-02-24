pipeline {
  agent {
    node {
      label '\'salve\''
    }
    
  }
  stages {
    stage('checkout') {
      steps {
        git(url: 'ssh://git@pangu.bldz.com:10022/core-service/commodity-soa.git', credentialsId: 'gitlab', branch: '$gitbranch')
      }
    }
  }
  environment {
    gitbranch = 'release/pre'
  }
}