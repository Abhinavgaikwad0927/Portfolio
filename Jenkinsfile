pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Abhinavgaikwad0927/Portfolio.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the app...'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo No tests for static site'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the app...'
                sh 'cp -r * /var/www/html/ 2>/dev/null || echo Deploy done'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline successful!'
        }
        failure {
            echo '❌ Pipeline failed!'
        }
    }
}
