node {
    checkout scm

    docker.withRegistry('https://index.docker.io/v1/', 'agung-docker') {

        def customImage = docker.build("agung3wi/go-helloworld:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}