pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-python-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker rm -f my-container || true'
                sh 'docker run -d -p 5000:5000 --name my-container my-python-app'
            }
        }

    }
}
