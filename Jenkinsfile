pipeline {
    agent any // Use any available agent
    
    tools {
        maven 'Maven' // Make sure Maven is configured in Jenkins
        jdk 'Java 11' // Ensure Java 11 is configured in Jenkins
    }
    
    stages {
        stage('Clone Repository') {
            steps {
                // Clone the GitHub repository
                git url: 'https://github.com/your-username/my-java-app.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                // Build the project using Maven
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                // Run the tests using Maven
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                // Package the application into a JAR file
                sh 'mvn package'
            }
        }
    }
    
    post {
        success {
            echo 'Build and Test Completed Successfully!'
        }
        failure {
            echo 'Build or Test Failed.'
        }
    }
}

