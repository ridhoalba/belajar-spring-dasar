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
        stage('Build'){
            steps {
                echo"build"
            }
        }
        stage('Test'){
            steps{
                echo "Test"
            }
        }
        steps('Deploy'){
            echo "deploy"
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
