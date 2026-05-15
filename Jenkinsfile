pipeline {
    agent any

    tools {
        nodejs 'NodeJS'
    }

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/OmTiwari2003/react-jenkins-apps.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'cd react-jenkins-app && npm install'
            }
        }

        stage('Build React App') {
            steps {
                bat 'cd react-jenkins-app && npm run build'
            }
        }

        stage('Deploy') {
            steps {
                bat 'xcopy react-jenkins-app\\build C:\\deploy\\react-app\\ /E /I /Y'
            }
        }
    }
}