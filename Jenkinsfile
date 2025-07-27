pipeline {
    agent {
        label 'java-slave'
    }

    tools {
        maven 'maven-3.8.9'
        jdk 'JDK-17'
    }

    environment {
        APPLICATION_NAME = "eureka"
        DOCKER_IMAGE_NAME = "your-dockerhub-username/eureka" // Replace with your Docker image name
        DOCKER_REGISTRY = "docker.io"  // Replace with your Docker registry if using a private one
    }

    stages {
        stage('Build') {
            steps {
                echo "************* Building ${env.APPLICATION_NAME} Application ***************"
                sh 'mvn clean package -DskipTests=true'
            }
        }

        stage('Build & Deploy Docker Image') {
            steps {
                echo "************* Building Docker Image ***************"
                script {
                    // Build Docker image
                    sh """
                        docker build -t ${env.DOCKER_IMAGE_NAME}:${env.BUILD_NUMBER} .
                    """

                    // Log in to Docker registry
                    withCredentials([usernamePassword(credentialsId: 'dockerhub-credentials', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD')]) {
                        sh """
                            echo \$DOCKER_PASSWORD | docker login -u \$DOCKER_USERNAME --password-stdin
                        """
                    }

                    // Push Docker image to registry
                    sh """
                        docker push ${env.DOCKER_IMAGE_NAME}:${env.BUILD_NUMBER}
                    """
                }
            }
        }
    }
}
