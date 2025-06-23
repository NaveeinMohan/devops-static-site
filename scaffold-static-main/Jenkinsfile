pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/NaveeinMohan/devops-static-site.git'
            }
        }

        stage('Print Message') {
            steps {
                bat 'echo Hello from Jenkins Pipeline!'
            }
        }
    }
}
