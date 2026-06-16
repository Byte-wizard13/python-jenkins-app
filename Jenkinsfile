pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // कोड GitHub वरून क्लोन करणे
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                # डिपेंडन्सी इन्स्टॉल करणे
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                # टेस्ट केसेस रन करणे
                sh 'pytest'
            }
        }
    }
}