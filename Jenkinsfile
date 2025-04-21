pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Sharmaujjawal123/Jenkins_test.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-node-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
     bat '''
            docker rm -f my-con_jen || echo "Container not found"
            docker run -d --name my-con_jen -p 3000:3000 my-node-image
        '''
            }
        }
    }
}
