node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'DH') {
        
    docker.withTool('docker') { //whatever docker commands you wish to run here 
    def customImage = docker.build("kiyange26773/dockerwebapp")

        /* Push the container to the custom Registry */
        customImage.push()
    }
        
    }
}
