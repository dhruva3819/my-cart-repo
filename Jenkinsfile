pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "**** Coming from Build stage *********"
            }
        }
        stage('grovystage') {
            steps {
                script {
                    // Correct variable declaration with single =
                    def course = "k8s"

                    // Correct if-else syntax with brackets for multi-line blocks
                    if (course == "k8s") {
                        println("thanks for enrolling")
                    } else {
                        println("do enroll for k8s")
                    }

                    // Print with variable interpolation
                    println("Thanks for enrolling to ${course} course")
                }
            }
        }
    }
}
