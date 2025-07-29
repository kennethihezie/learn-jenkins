pipeline {
    agent any 

    tools {
        nodejs 'Nodejs_24'
    }

    environment {
        PORT=3000
    }

    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main', url: 'https://github.com/kennethihezie/learn-jenkins.git'
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run tests') {
            steps {
                sh 'npm run test'
            }
        }

        stage('Build application') {
            steps {
                sh 'npm run build'
            }
        }
    }
}