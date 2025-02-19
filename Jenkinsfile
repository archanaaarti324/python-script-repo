pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the repository...'
                git credentialsId: 'github-credentials', 
                    url: 'https://github.com/archanaaarti324/python-script-repo.git', 
                    branch: 'python'
            }
        }

        stage('Build') {
            steps {
                script {
                    echo 'Starting the Build Process...'
                    if (isUnix()) {
                        echo 'Simulating: Running build.sh on Unix'
                    } else {
                        echo 'Simulating: Running build.bat on Windows'
                    }
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running Tests...'
                    if (isUnix()) {
                        echo 'Simulating: Running run_tests.sh on Unix'
                    } else {
                        echo 'Simulating: Running run_tests.bat on Windows'
                    }
                }
            }
        }
		stage('Deploy') {
            steps {
                script {
                    echo 'Running Tests...'
                    if (isUnix()) {
                        echo 'Simulating: Running deploy.sh on Unix'
                    } else {
                        echo 'Simulating: Running deploy.bat on Windows'
                    }
                }
            }
        }
    }
}
