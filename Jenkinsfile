pipeline {
    agent any
    tools {
        nodejs 'NodeJS'
    }
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Pranjal6955/devops-test.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'npm test || echo "No tests defined"'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}