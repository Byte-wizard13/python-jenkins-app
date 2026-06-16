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
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // थेट pytest ऐवजी python च्या मॉड्यूल थ्रू रन करणे (विंडोजसाठी सर्वोत्तम)
                bat 'python -m pytest'
            }
        }
    }
}