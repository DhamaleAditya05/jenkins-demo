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
                sh 'docker run my-python-app'
            }
        }

    }
}
