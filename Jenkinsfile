pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                bat 'echo Build step running'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'echo Test step running'
            }
        }

        stage('Code Coverage') {
            steps {
                echo 'Generating coverage...'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                echo 'Running SonarQube...'
            }
        }

        stage('Deliver') {
            steps {
                echo 'Delivering artifact...'
            }
        }

        stage('Deploy to Dev Env') {
            steps {
                echo 'Deploying to Dev...'
            }
        }

        stage('Deploy to QAT Env') {
            steps {
                echo 'Deploying to QAT...'
            }
        }

        stage('Deploy to Staging Env') {
            steps {
                echo 'Deploying to Staging...'
            }
        }

        stage('Deploy to Production Env') {
            steps {
                echo 'Deploying to Production...'
            }
        }
    }
}