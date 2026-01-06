pipeline {
    agent any

    stages {
        stage('Setup Python Environment') {
            steps {
                bat '''
                python3 --version
                python3 -m venv venv
                . venv/bin/activate
                pip install --upgrade pip
                pip install -r requirements.txt
                '''
            }
        }

        stage('Run Tests') {
            steps {
                bat '''
                . venv/bin/activate
                pytest
                '''
            }
        }
    }
}
