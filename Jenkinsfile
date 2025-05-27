pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'github-creds', url: 'https://github.com/Zooiiee/simple-web-app.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo 'Nothing to build for static HTML, skipping...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying index.html to local HTTP server...'
                sh '''
                  mkdir -p /var/www/html
                  cp index.html /var/www/html/index.html
                '''
            }
        }
    }
}
