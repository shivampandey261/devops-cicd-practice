pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Source code checkout stage'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                bat 'echo Build successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing application...'
                bat 'echo All tests passed'
            }
        }

        stage('Environment Check') {
            steps {
                bat 'whoami'
                bat 'hostname'
                bat 'java -version'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment successful!'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
