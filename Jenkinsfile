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
                // 'py -m' विंडोजवर आपोआप योग्य पाथ शोधून काढते
                bat 'py -m pip install --upgrade pip'
                bat 'py -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'py -m pytest'
            }
        }
    }
}