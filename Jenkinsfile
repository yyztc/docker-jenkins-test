pipeline {
  agent any
  stages {
    stage("verify tooling..") {
      steps {
        sh '''
        /usr/local/bin/docker version
        /usr/local/bin/docker info
        docker compose version
        curl --version
        jq --version
        '''
      }
    }
  }
}
