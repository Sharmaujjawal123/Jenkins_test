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
                bat 'docker build -t jenkins_test .'
            }
        }

        stage('Run Docker Container') {
            steps {
     bat '''
            docker rm -f my_con_jen
            docker run -d --name my_con_jen -p 82:82 jenkins_test
        '''
            }
        }
    }
}
