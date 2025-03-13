pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ main.cpp -o PES1UG22CS312'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS312'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
