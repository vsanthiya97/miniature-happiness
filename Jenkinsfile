pipeline {
    agent any
    stages {
        stage('checkout scm stage,') {
            steps {
            checkout scm
            }
        }
        stage('Build docker') {
            steps {
            script {
                withCredentials([gitUsernamePassword(credentialsId: 'santhiya-git',
                 gitToolName: 'git-tool')]) {
                    sh 'git fetch --all'
                }

                //def branchname = sh(script: 'git rev-parse --abbrev-ref HEAD', returnStdout: true).trim()
                //echo $branchname
                app = docker.build("santhiya_docker")
                }
            }
        }
    }
}