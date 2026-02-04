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
                echo "Analyzing code quality in ${ENV} environment"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying ${APP_NAME}"
            }
        }
    }
}
