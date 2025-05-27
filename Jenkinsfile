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
                echo 'Deploying to Jenkins workspace folder...'
                sh 'mkdir -p deploy'
                sh 'cp index.html deploy/index.html'
            }
        }
    }
}
