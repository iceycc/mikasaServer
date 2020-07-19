pipeline {
    agent {
        docker {
            image 'node:10-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('ha ha') { 
            steps {
                sh 'echo 001' 
            }
        }
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('stop') { 
            steps {
                sh 'npm run stop' 
            }
        }
        stage('start') { 
            steps {
                sh 'npm run start' 
            }
        }
    }
}