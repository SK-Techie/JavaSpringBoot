pipeline {
    agent any

    tools {
        jdk 'Java 21'
        maven 'Maven 3.9.5'
    }

    stages {
        stage('Build with Maven') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy to EC2') {
            steps {
                echo 'Deployment logic goes here...'
            }
        }
    }
}
