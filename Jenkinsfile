pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/Zooiiee/simple-web-app.git', branch: 'main', credentialsId: 'github-creds'
            }
        }

        stage('Build') {
            steps {
                echo 'Static site - no build step needed.'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Copying files to Apache web server folder...'
                // You might need to run as root or configure permissions properly
                sh 'mkdir -p /var/www/html'
                sh 'cp index.html /var/www/html/index.html'
            }
        }
    }
}
