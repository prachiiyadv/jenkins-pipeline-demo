
pipeline {
    agent any

    environment {
        REPO_URL = 'https://github.com/prachiiyadv/jenkins-pipeline-demo.git'
        BRANCH   = 'main'
    }

    stages {

        stage('Clone Repository') {
            steps {
                echo "Cloning repository from GitHub..."
                bat "git clone -b %BRANCH% %REPO_URL% repo"
            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
                bat "echo Build step running..."
                bat "cd repo && echo npm install or other build commands here"
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                bat "echo Unit tests or shell commands to test project"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                bat "echo Deploy commands (dummy) here"
            }
        }

        stage('Cleanup') {
            steps {
                echo "Cleaning workspace..."
                bat "rmdir /s /q repo"
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully!"
        }
        failure {
            echo "Pipeline failed. Check logs."
        }
    }
}
