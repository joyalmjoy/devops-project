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
                bat 'echo Build running'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing project...'
                bat 'echo Tests passed'
            }
        }

        stage('Code Coverage') {
            steps {
                echo 'Coverage step'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                echo 'SonarQube step'
            }
        }

        stage('Deliver') {
    steps {
        echo 'Creating artifact...'
        writeFile file: 'artifact.txt', text: 'This is my build artifact'
        archiveArtifacts artifacts: 'artifact.txt', fingerprint: true
    }
}



        stage('Deploy to Dev Env') {
            steps {
                echo 'Deploying to Dev'
            }
        }

        stage('Deploy to QAT Env') {
            steps {
                echo 'Deploying to QAT'
            }
        }

        stage('Deploy to Staging Env') {
            steps {
                echo 'Deploying to Staging'
            }
        }

        stage('Deploy to Production Env') {
            steps {
                echo 'Deploying to Production'
            }
        }
    }
}
