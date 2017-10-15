pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t mateusprado/raspstack.org .'
        sh 'env'
      }
    }
    stage('Tests') {
      steps {
        sh 'ls -l'
      }
    }
    stage('Approval') {
      steps {
        input 'Você aprova isto para deploy?'
      }
    }
    stage('Deploy') {
      steps {
        sh 'pwd'
      }
    }
  }
  environment {
    MYSQL_USER = 'root'
  }
}