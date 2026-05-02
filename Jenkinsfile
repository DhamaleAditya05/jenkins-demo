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
                sh '''
                python3 -m venv venv
                . venv/bin/activate
                pip install -r requirements.txt
                '''
            }
        }

        stage('Run Application') {
            steps {
                sh '''
                . venv/bin/activate
                python app.py
                '''
            }
        }

    }
}
