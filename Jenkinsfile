pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t quote-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 5001:5000 quote-app'
            }
        }
    }
}