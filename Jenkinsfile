pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "**** Coming from Build stage *********"
            }
        }
        stage ('grovystage') {
            steps {
                script {
                    // i want to define a variable
                // def variablename = "value"
                def course == "k8s"

                // if condition
                if (course == "k8s")
                println("thanks for enrolling")
                else
                    println("do enroll for k8s")
                //println("Thanks for enrolling to ${course} course")

                }
                
            }
        }
    }
}

// ${course} , ${env,course}, ${params,course}

// ${course} , ${env,course}, ${params,course}
