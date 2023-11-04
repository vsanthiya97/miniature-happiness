pipeline {
    //agent {
    //    docker { image 'node:20.9.0-alpine3.18' }
    //}
    stages {
        stage('Build') {
            script{
                 app = docker.build("santhiya_docker")
                }
        }
    }
}