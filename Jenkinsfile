pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/Zooiiee/simple-web-app.git', branch: 'main'
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
                sh '''
                  sudo mkdir -p /var/www/html
                  sudo cp -r * /var/www/html/
                '''
            }
        }
    }
}
