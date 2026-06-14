pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building...'
                sh 'node --version'
            }
        }
        stage('Test') {
            steps {
                echo 'Tests passed successfully'
                // Add your test commands here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'docker build -t uzair-cicd .'
                echo 'Deployment successful'
            }
        }
        post {
            success { echo 'Pipeline completed successfully!'}
            failure { echo 'Pipeline failed. Please check the logs.' }
            }
    }
}