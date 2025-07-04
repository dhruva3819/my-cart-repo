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
                // i want to define a variable
                // def variablename = "value"
                def course = "k8s"
                println("Tthanks for enrolling to ${course} course")
            }
        }
    }
}

// ${course} , ${env,course}, ${params,course}
