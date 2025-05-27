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
                echo 'Nothing to build for HTML, skipping...'
            }
        }

        stage('Deploy') {
    echo 'Deploying to local HTTP server...'
    sh './deploy.sh'  // or whatever shell command you want to run on Linux
}
    }
}
