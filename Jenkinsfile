pipeline {
    agent any

    stages {
        stage('Clone Info') {
            steps {
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Run App') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}
