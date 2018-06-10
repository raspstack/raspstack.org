pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "iniciando o build"'
        sh 'ls -l'
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
