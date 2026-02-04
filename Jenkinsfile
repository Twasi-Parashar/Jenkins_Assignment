pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building application'
            }
        }

        stage('Test') {
    steps {
        sh 'mvn test'
    }
}


        stage('Deploy') {
            steps {
                echo 'Deploying application'
            }
        }

        stage('Code Quality') {
    steps {
        echo 'Analyzing code quality using SonarQube'
    }
}

    }
}
