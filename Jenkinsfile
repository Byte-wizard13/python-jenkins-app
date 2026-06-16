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
                // pip चा अचूक पाथ वापरून डिपेंडन्सी इन्स्टॉल करणे
                bat '"C:\\Users\\ADMIN\\AppData\\Local\\Programs\\Python\\Python312\\Scripts\\pip.exe" install --upgrade pip'
                bat '"C:\\Users\\ADMIN\\AppData\\Local\\Programs\\Python\\Python312\\Scripts\\pip.exe" install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // pytest चा अचूक पाथ वापरून टेस्ट रन करणे
                bat '"C:\\Users\\ADMIN\\AppData\\Local\\Programs\\Python\\Python312\\Scripts\\pytest.exe"'
            }
        }
    }
}