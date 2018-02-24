pipeline {
  agent {
    node {
      label 'salve'
    }
    
  }
  stages {
    stage('checkout') {
      agent {
        node {
          label 'salve'
        }
        
      }
      environment {
        gitbranch = 'release/pre'
        Name = 'origin'
        Refspec = '+refs/heads/*:refs/remotes/origin/*'
      }
      steps {
        git(url: 'ssh://git@pangu.bldz.com:10022/core-service/commodity-soa.git', credentialsId: 'gitlab', branch: '$gitbranch', poll: true, changelog: true)
      }
    }
  }
  environment {
    gitbranch = 'release/pre'
  }
}