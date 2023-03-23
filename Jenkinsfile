pipeline {
  agent {label 'macos'}
  stages {
    stage('Verify tooling') {
      steps {
        sh '''
        /usr/local/bin/docker version
        /usr/local/bin/docker info
        #/usr/local/bin/docker-compose version
        /usr/bin/curl  --version
        '''
      }
    }
    stage('Start container') {
      steps {
        sh 'docker compose up -d --no-color --wait'
        sh 'docker compose ps'
      }
    }
  }
}
