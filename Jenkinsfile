pipeline {
    agent { label 'devops1-ryan' }

    stages {
        stage('Build Apps') {
            steps {
                sh '''cd app
                npm install'''
            }
        }

        stage('Testing Apps') {
            steps {
                echo 'test apps'
            }
        }

        stage('Code Scan') {
            steps {
                echo 'code scan'
            }
        }

        stage('Build Images') {
            steps {
                echo 'build images'
            }
        }

        stage('Push Images') {
            steps {
                echo 'push images'
            }
        }

        stage('Deploy Apps') {
            steps {
                echo 'deploy apps'
            }
        }
    }
}