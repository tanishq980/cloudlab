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
                echo 'STAGE 2: Build'
                echo '================================'

                bat 'echo Build completed successfully!'
            }
        }

        stage('Run') {
            steps {
                echo '================================'
                echo 'STAGE 3: Run'
                echo '================================'

                bat 'echo Application is running...'
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
            echo '================================'
            echo 'Pipeline completed successfully!'
            echo '================================'
        }

        failure {
            echo '================================'
            echo 'Pipeline failed!'
            echo '================================'
        }
    }
}
