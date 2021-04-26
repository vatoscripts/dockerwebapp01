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

 stage('Publish to DH') { 

            steps { 

                script { 
                  docker.withRegistry('https://registry.hub.docker.com', 'DH') {
                       dockerImage.push()
                      def customImage = docker.build("kiyange26773/webapp:v1")

        /* Push the container to the custom Registry */
                      customImage.push()
                     }
                   

                } 

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

  }
}
