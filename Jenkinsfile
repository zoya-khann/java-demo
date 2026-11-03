pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat '"C:\\Users\\sameer\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" helloworld.py'
            }
        }
        stage('Test') {
            steps {
                bat 'echo "Running Tests..."'
            }
        }
        stage('Deploy') {
            steps {
                bat 'echo "Deploying application..."'
            }
        }
        stage('End') {
            steps {
                bat 'echo "Pipeline Completed successfully"'
            }
        }
    }
}
