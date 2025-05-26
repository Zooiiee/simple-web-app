pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'github-creds', url: 'https://github.com/YOUR_USERNAME/simple-web-app.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Nothing to build for HTML, skipping...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to local HTTP server...'
                bat 'copy index.html "C:\\inetpub\\wwwroot\\index.html" /Y'
            }
        }
    }
}
