pipeline {
    agent {
        docker {
            image 'node:10-alpine' 
            args '-p 7001:7001' 
        }
    }
    stages {
        stage('001') { 
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                '''
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