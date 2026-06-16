pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                // 'python -m pip' वापरल्याने पाथची समस्या सुटते
                bat 'python -m pip install --upgrade pip'
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // pytest थेट रन न करता python द्वारे रन करणे
                bat 'python -m pytest'
            }
        }
    }
}