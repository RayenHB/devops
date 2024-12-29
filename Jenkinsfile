pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/RayenHB.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t my-app .'
            }
        }
        stage('Test') {
            steps {
                sh 'docker run my-app test-command'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 80:80 my-app'
            }
        }
    }
}
