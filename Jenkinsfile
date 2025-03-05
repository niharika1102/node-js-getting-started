pipeline {
    agent any

    environment {
        NODE_HOME = tool('NodeJS')  // Correct way to define tool
        PATH = "${NODE_HOME}/bin:${env.PATH}" // Proper PATH assignment
    }

    stages {
        stage('Install Dependencies') {
            steps {
                bat 'npm install' // Use sh 'npm install' for Linux
            }
        }

        stage('Build') {
            steps {
                bat 'npm run build' // Use sh 'npm run build' for Linux
            }
        }

        stage('Test') {
            steps {
                bat 'npm test' // Use sh 'npm test' for Linux
            }
        }

        stage('Deploy') {
            steps {
                bat 'npm start' // Use sh 'npm start' for Linux
            }
        }
    }
}
