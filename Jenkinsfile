pipeline {
  agent any
  stages {
    def app     
      stage('Clone repository') {               
             
            checkout scm    
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

    stage('App Deploy') {
      steps {
        echo 'Deployed!'
      }
    }

    stage('message') {
      steps {
        echo 'message'
      }
    }
    
        stage('Push... image') {
             docker.withRegistry('https://registry.hub.docker.com', 'DH') {            
             app.push("${env.BUILD_NUMBER}")            
             app.push("latest")        
              }    
           }

  }
}
