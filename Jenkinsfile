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
    }

    stages {
        stage('Build') {
            steps {
                echo "************* Building ${env.APPLICATION_NAME} Application ***************"
                sh 'mvn clean package -DskipTests=true'
            }
        }

        stage('Sonar Scan') {
            steps {
                echo "********** Starting SonarQube scan ************"
                sh """
                    mvn clean verify sonar:sonar \
                    -Dsonar.projectKey=i27-eureka
                """
            }
        }

        stage('BuildFormat') {
            steps {
                echo '************ Docker build and push stage ************'
                // Add Docker build and push commands here
            }
        }
    }
}
