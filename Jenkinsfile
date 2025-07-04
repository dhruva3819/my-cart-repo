pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Running build stage...'
                sh 'echo Building your project!'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo Testing...'
            }
        }
    }
}
