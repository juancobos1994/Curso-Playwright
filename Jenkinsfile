pipeline {
    agent any
    stages {
        stage('Pull') {
            steps {
                sh 'docker pull auntoracharja/letcode-smoke-and-api-test-automation:latest'
            }
        }
        stage('Run') {
            steps {
                sh 'npx -y playwright@1.42.1 install --with-deps'
                sh 'npm run test'
                sh 'docker run auntoracharja/letcode-smoke-and-api-test-automation:latest'
            }
        }
    }
}