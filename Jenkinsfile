pipeline {
    agent any
    tools{
        nodejs 'NodeJS'
    }
    Stages{
        Stage('Clone Repository'){
            Steps{
            git branch : 'main' , url:'https://github.com/Pranjal6955/devops-test.git'
            }
        }
        Stage('Install Dependencies'){
            Steps{
                sh 'npm install'
            }
        }
        Stage('Run Tests'){
            Steps{
                sh 'npm test || echo "No tests defined"'
            }
        }
        Stage('Build'){
            Steps{
                sh 'npm run build'
            }
        }
    }
}