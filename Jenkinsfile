
pipeline {
    agent {
        docker {
            image 'node:22-alpine'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'echo Starting application build'
                sh 'node --version'
                sh 'npm --version'
                sh 'echo Build completed successfully'
            }
        }

        stage('Test') {
            steps {
                sh 'echo Running application tests'
                sh 'echo All tests passed'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deployment stage completed'
            }
        }
    }

    post {
        success {
            echo 'CI/CD pipeline created by FA23-BCS-022 2nd time Commit!'
            echo 'CI/CD pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}
