pipeline {
  agent any
  stages {
    stage('build') {
      agent {
        node {
          label 'salve'
        }
        
      }
      steps {
        git(url: 'http://pangu.bldz.com:10081/business-service/mall-basic-soa.git', branch: 'release/pre', credentialsId: 'gitlab')
        sh 'mvn clean package -Dmaven.test.skip=true'
      }
    }
    stage('UT') {
      steps {
        echo 'ingore unit test!'
      }
    }
    stage('deploy') {
      steps {
        sh '''echo "run deploy_edas.sh"
echo "deploy war via EDAS on server!"'''
      }
    }
  }
  environment {
    gitbranch = 'release/pre'
  }
}