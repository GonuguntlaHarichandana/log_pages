pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'cea236ce-0912-4867-8d4f-9f4029216aff', url: 'https://github.com/GonuguntlaHarichandana/log_pages.git']]])
            }
        }
        stage('Build') {
            steps {
                bat 'python mamage.py runserver'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
