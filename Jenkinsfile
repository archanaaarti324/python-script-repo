pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-repo/python-ci-cd.git'
            }
        }

        stage('Build') {
            steps {
                bat 'python --version'
            }
        }

        stage('Test') {
            steps {
                bat 'pytest --junitxml=report.xml'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo "Deployment step: Copying files to server..."'
            }
        }
    }
}
