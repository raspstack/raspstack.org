pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "iniciando o build"'
        sh 'docker build -t raspstack.org .'
      }
    }
    stage('Tests') {
      steps {
        sh 'pwd'
      }
    }
    stage('Aprovação') {
      steps {
        input 'Aprova o Deploy?'
      }
    }
    stage('Dpeloy') {
      steps {
        sh 'echo "fazendo deploy"'
      }
    }
  }
  post {
    always {
      junit 'testete'
    }
  }
}
