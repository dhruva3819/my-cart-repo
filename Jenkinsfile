pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                script {
                    retry(3) {
                        echo "Welcome to jenkins pipeline"
                        error "This will give some error"
                    }
                    // This won't be executed if retry fails
                    echo "***** Printing after multiple retries ******"
                }
            }
        }
    }
}
