pipeline {
    agent any

    tools {
        nodejs 'NodeJS'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'prod',
                url: 'https://github.com/Vimalraj-7202/devops_frontend.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'chmod +x node_modules/.bin/vite'
                sh 'npm run build'
            }
        }
    }
}