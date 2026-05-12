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
                sh 'sudo docker build -t java-maven-app .'
            }
        }

        stage('Verify Docker Image') {
            steps {
                sh 'sudo docker images'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'sudo docker run -d --name java-container java-maven-app'
            }
        }
    }
}
