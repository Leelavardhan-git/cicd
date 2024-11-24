pipeline {
    agent any

    environment {
        APP_NAME = 'my-sample-app'
    }

    stages {
        stage('Clone Repository') {
            steps {
                echo 'Cloning the repository...'
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'echo "Simulating build process..."' // Replace with actual build command
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "Simulating test process..."' // Replace with actual test command
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'echo "Simulating deployment process..."' // Replace with actual deploy command
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
