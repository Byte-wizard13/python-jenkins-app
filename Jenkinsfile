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
                // तुमच्या सिस्टीममधील युझर प्रोफाईलचा वापर करून थेट Python रन करणे
                bat 'cmd /c "FOR /F "tokens=*" %i IN (\'where python\') DO @"%i" -m pip install --upgrade pip"'
                bat 'cmd /c "FOR /F "tokens=*" %i IN (\'where python\') DO @"%i" -m pip install -r requirements.txt"'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'cmd /c "FOR /F "tokens=*" %i IN (\'where python\') DO @"%i" -m pytest"'
            }
        }
    }
}