pipeline {
    agent any

    environment {
        APP_NAME = "StudentApp"
        ENV = "DEV"
    }

    stages {

        stage('Build') {
            steps {
                echo "Building ${APP_NAME}"
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Code Quality') {
            steps {
                echo "Analyzing code quality using SonarQube"
            }
        }

        stage('Credentials Demo') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'demo-creds',
                    usernameVariable: 'USER',
                    passwordVariable: 'PASS'
                )]) {
                    echo 'Credentials used securely'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying ${APP_NAME}"
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
        always {
            echo 'Pipeline finished'
        }
    }
}
