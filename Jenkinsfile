pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                retry(3) {
                    echo "Welcome to jenkins pipeline"
                    error "This will give give some error"
                }
                echo "***** Printing after mulitiple retries ******"
            }
                
            }
        }
    }
}
