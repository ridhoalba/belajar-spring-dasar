pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }
    stages {
        stage('Hello') {
            steps {
                echo "Belajar Pipeline"
            }
            steps {
                ./mvnw compile
            }
            steps {
                ./mvnw test
            }
        }
    }
    post {
        always {
            echo "I will say hello again!"
        }
        success {
            echo "Yey, Success"
        }
        failure {
            echo "oh no, failure"
        }
        cleanup {
            echo "don't care success or error"
        }
    }
}
