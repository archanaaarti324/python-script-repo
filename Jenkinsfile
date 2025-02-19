ho pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                 git credentialsId: 'github-credentials', url: 'https://github.com/archanaaarti324/python-script-repo.git', branch: 'python'
            }
        }

        stage('Build') {
            steps {
                bat 'echo "Building"'

            }
        }

        stage('Test') {
            steps {
                bat 'echo "pytest"'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo "Deployment step: Copying files to server..."'
            }
        }
    }
}
