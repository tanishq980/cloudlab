pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo '================================'
                echo 'STAGE 1: Getting code from Git'
                echo '================================'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo '================================'
                echo 'STAGE 2: Compiling Java files'
                echo '================================'

                bat 'javac Calculator.java'
            }
        }

        stage('Run') {
            steps {
                echo '================================'
                echo 'STAGE 3: Running Java program'
                echo '================================'

                bat 'java Calculator'
            }
        }

        stage('Deploy') {
            steps {
                echo '================================'
                echo 'STAGE 4: Deploy'
                echo '================================'

                bat 'echo Deployment successful!'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
