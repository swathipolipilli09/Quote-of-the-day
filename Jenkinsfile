pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/swathipolipilli09/Quote-of-the-day.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t quote-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 5000:5000 quote-app'
            }
        }
    }
}