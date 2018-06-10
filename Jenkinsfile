pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "iniciando o build"'
        sh 'docker build -t raspstack.org .'
        sh '/usr/local/share/gems/gems/fpm-1.10.0/bin/fpm -m "CodeOps, <help@codeops.com.br>" --url "https://codeops.com.br" --description "A test package" -a noarch -s dir -t rpm -n raspstack --rpm-user root --rpm-group root -v 1.0.0 --prefix /opt/raspstack/ .'
      }
    }
    stage('Tests') {
      steps {
        sh 'docker run -d raspstack.org'
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
