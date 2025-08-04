pipeline { 
    agent any

    tools {
        maven 'Maven 3.9.5'
        jdk 'Java version: 17.0.16'
    }

    environment {
        DEPLOY_DIR = '/home/ec2-user/app'
    }

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/SK-Techie/JavaSpringBoot.git'
            }
        }

        stage('Build with Maven') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy to EC2') {
            steps {
                sh '''
                mkdir -p $DEPLOY_DIR
                cp targe
