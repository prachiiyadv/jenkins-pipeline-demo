pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/prachiiyadv/jenkins-pipeline-demo/tree/main'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building app..."'
                sh 'sleep 1'
                sh 'echo "Build completed!"'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
                sh 'sleep 1'
                sh 'echo "All tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying app..."'
                sh 'sleep 1'
                sh 'echo "App deployed successfully!"'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
