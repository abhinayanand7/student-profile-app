pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/abhinayanand7/student-profile-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh '/usr/local/bin/docker build -t student-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh '/usr/local/bin/docker stop student-container || true'
                sh '/usr/local/bin/docker rm student-container || true'
            }
        }

        stage('Run Container') {
            steps {
                sh '/usr/local/bin/docker run -d -p 5002:5000 --name student-container student-app'
            }
        }
    }
}