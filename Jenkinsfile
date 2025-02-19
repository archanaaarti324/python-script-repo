pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                 git credentialsId: 'github-credentials', url: 'https://github.com/archanaaarti324/python-script-repo.git', branch: 'python'
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
