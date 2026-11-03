pipeline {
    agent any
    stages {
        stage('Build') {
            parallel {
                stage('Build Stage') {
                    steps {
                        bat '"C:\\Users\\sameer\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" helloworld.py'
                        bat 'echo "Build Version 1.0" > build-info.txt'
                    }
                }
                stage('Archive the artifacts') {
                    steps {
                        archiveArtifacts artifacts: 'build-info.txt', allowEmptyArchive: true
                    }
                }
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
                bat 'echo "Pipeline completed successfully"'
            }
        }
    }
}
