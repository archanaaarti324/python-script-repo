pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'github-credentials', 
                    url: 'https://github.com/archanaaarti324/python-script-repo.git', 
                    branch: 'python'
            }
        }

       stage('Build') {
            steps {
                script {
                    if (isUnix()) {
                        sh './build.sh'  // Runs on Linux/macOS
                    } else {
                        bat 'build.bat'  // Runs on Windows
                    }
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    if (isUnix()) {
                        sh './run_tests.sh'
                    } else {
                        bat 'run_tests.bat'
                    }
                }
            }
        }

        
