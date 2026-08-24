pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'STAGE 1: Building Java Program'
                bat 'javac Calculator.java CalculatorTest.java'
                echo 'Build Successful!'
            }
        }

        stage('Test') {
            steps {
                echo 'STAGE 2: Testing Calculator'
                bat 'java CalculatorTest'
                echo 'All Tests Completed!'
            }
        }

    }

    post {
        success {
            echo 'PIPELINE SUCCESS!'
        }

        failure {
            echo 'PIPELINE FAILED!'
        }
    }
}
