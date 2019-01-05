pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 4000:4000'
    }
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Deliver') { 
      steps {
        sh 'node node_modules/hexo/bin/hexo server -p 4000'
      }
    }
  }
}