pipeline {
    agent any

    stages {

        stage('Checkout Info') {
            steps {
                sh 'echo "Workspace info:"'
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Environment Check') {
            steps {
                sh 'echo "Checking Python version..."'
                sh 'python3 --version'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'echo "Installing dependencies (if any)..."'
            }
        }

        stage('Run Application') {
            steps {
                sh 'echo "Running app..."'
                sh 'python3 app.py'
            }
        }

    }
}
