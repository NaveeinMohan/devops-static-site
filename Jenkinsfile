pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/NaveeinMohan/devops-static-site.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build("static-site")
                }
            }
        }

        stage('Run Container') {
            steps {
                sh "docker run -d -p 8080:80 --name static-site-container static-site || echo 'Container may already be running'"
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}