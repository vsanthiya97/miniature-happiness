pipeline {
    agent any
    stages {
        stage('checkout scm stage,') {
            steps {
            checkout scm
            }
        }
        stage('Build') {
            steps {
            script {
                def branchname = sh(script: 'git rev-parse --abbrev-ref HEAD', returnStdout: true).trim()
                echo $branchname
                app = docker.build("santhiya_docker")
                }
            }
        }
    }
}