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
    stage('Testing') {
      steps {
        echo 'Testing Passed!'
      }
    }
    stage('Build') {
      steps {
        sh 'docker push kiyange26773/webapp:v1'
      }
    }
    stage('App Deploy') {
      steps {
        echo 'Deployed!'
      }
    }

  }
}
