pipeline {
    agent any
    tools { 
    nodejs "Node 21"
    }
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/SamsonKamunyu/gallery.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        
        stage('Test') {
            steps {
                sh 'npm test'
            }
            // post{If it Fails}
        }
        
        stage('Deploy To Render') {
            steps {
                sh 'node server.js'
            }
            // post{If it succeeds}
        }
    }
}

