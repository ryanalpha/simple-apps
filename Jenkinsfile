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
                sh '''cd app
                npm test'''
            }
        }

        stage('Code Scan') {
            steps {
                sh '''cd app
                sonar-scanner   -Dsonar.projectKey=simple-apps   -Dsonar.sources=.   -Dsonar.host.url=http://172.23.1.1:9000   -Dsonar.login=sqp_f38fd520a0668c9a22375a64eb5f18945b74d6cf'''
            }
        }

        stage('Build Images') {
            steps {
                sh '''
                docker compose build'''
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