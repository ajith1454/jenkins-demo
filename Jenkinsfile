pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/ajith1454/jenkins-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t ajith-devops-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 5000:5000 ajith-devops-app'
            }
        }

    }
}