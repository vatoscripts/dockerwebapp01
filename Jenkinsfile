node {

    checkout scm

<<<<<<< HEAD
    docker.withRegistry('https://registry.hub.docker.com', 'DH') {
=======
    docker.withRegistry('https://registry.hub.docker.com', 'dockerHUB') {
>>>>>>> 271025ab5e83735935f93db9d452d67551a866a9

        def customImage = docker.build("kiyange26773/dockerwebapp")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
