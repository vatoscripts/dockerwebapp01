pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        echo 'Init...'
      }
    }

    stage('Build') {
      steps {
        sh 'docker build . -t kiyange26773/webapp:v1'
      }
    }

  }
}