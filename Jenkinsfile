pipeline {
    agent any
    stages {
        stage('Build') {
            script{
                 app = docker.build("santhiya_docker")
                }
        }
    }
}