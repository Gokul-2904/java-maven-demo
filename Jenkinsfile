pipeline {
    agent any

    stages {

        stage('Build Maven Project') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t java-maven-app .'
            }
        }

        stage('Verify Docker Image') {
            steps {
                sh 'docker images'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d --name java-container java-maven-app'
            }
        }
    }
}
