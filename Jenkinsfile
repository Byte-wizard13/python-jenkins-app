pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Setup Virtual Environment') {
            steps {
                // १. मघाशी मिळालेला Windows App शॉर्टकट वापरून व्हर्च्युअल एन्व्हायरनमेंट तयार करणे
                bat 'C:\\Users\\ADMIN\\AppData\\Local\\Microsoft\\WindowsApps\\python.exe -m venv venv'
            }
        }

        stage('Install Dependencies') {
            steps {
                // २. तयार झालेल्या लोकल venv मधील pip वापरून डिपेंडन्सी इन्स्टॉल करणे
                bat 'venv\\Scripts\\pip install --upgrade pip'
                bat 'venv\\Scripts\\pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // ३. लोकल venv मधील pytest वापरून टेस्ट रन करणे
                bat 'venv\\Scripts\\pytest'
            }
        }
    }
}