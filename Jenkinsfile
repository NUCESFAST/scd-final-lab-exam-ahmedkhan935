pipeline {
    agent any

    stages {
        stage('Checkout 1152') {
            steps {
                git 'https://github.com/NUCESFAST/scd-final-lab-exam-ahmedkhan935.git'
            }
        }

        stage('Dependency Installation 1152') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build Docker Images 1152') {
            steps {
                bat 'docker compose build'
            }
        }

      
        stage('Push Docker Image') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'docker-hub-credentials', usernameVariable: 'DOCKER_USER', passwordVariable: 'DOCKER_PASS')]) {
                    bat 'docker login -u %DOCKER_USER% -p %DOCKER_PASS%'
                    bat 'docker compose push'
                }
            }
        }
    }
}