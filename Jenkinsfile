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
        }
        stage('clean'){
            steps{
                ./mvnw clean
            }
        }
        stage('compiling'){
            steps{
                ./mvnw compile test-compile
            }
        }
        stage('test'){
            steps{
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
