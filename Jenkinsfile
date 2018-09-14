pipeline {
  agent {
    node {
      label 'php'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh './build'
        echo 'budowa'
      }
    }
    stage('Test') {
      steps {
        sh '''./deploy
'''
      }
    }
    stage('Deploy') {
      steps {
        sh './deploy.sh'
      }
    }
  }
  environment {
    ansiColor = 'xterm'
  }
}