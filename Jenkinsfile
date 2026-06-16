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
                // Windows साठी bat कमांडचा वापर
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // Windows साठी bat कमांडचा वापर
                bat 'pytest'
            }
        }
    }
}