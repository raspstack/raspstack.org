pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t mateusprado/raspstack.org .'
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
}