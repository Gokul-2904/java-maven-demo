pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning Repository'
            }
        }

        stage('Build Maven Project') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Verify Artifact') {
            steps {
                sh 'ls -l target'
            }
        }
    }
}
