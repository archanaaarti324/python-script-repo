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
                bat 'C:\Users\DELL\AppData\Local\Microsoft\WindowsApps\python.exe --version'
            }
        }

        stage('Test') {
            steps {
                bat echo 'pytest --junitxml_report_xml'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo "Deployment step: Copying files to server..."'
            }
        }
    }
}
