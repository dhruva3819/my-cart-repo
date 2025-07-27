pipeline {
    agent {
        label 'java-slave' 
    }
    stages {
        stage('build') {
            steps {
                echo "Build stage from feature branch"
            }
        }
        stage('Scans') {
            steps {
                echo "Scans stage from feature branch"
            }
        }
        stage('dockerbuild') {
            steps {
                echo "Docker stage from feature branch"
            }
        }
        stage('deployment') {
            steps {
                echo "Deploying stage from feature branch"
            }
        }
    }
}
