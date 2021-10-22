node {
    checkout scm

    docker.withRegistry('https://hub.docker.com', 'agung-docker') {

        def customImage = docker.build("go-helloworld:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
