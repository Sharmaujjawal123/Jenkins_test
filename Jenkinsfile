pipeline {
    agent any

    stages {
        stage('pull code from github') {
            steps {
                git branch: 'main', url:'https://github.com/Sharmaujjawal123/Jenkins_test.git'
            }
        }

        stage('Install dependency') {
            steps {
                
                bat 'npm install'
            }
        }

        stage('Restart Node.js Server') {
            steps {
               bat 'pm2 delete all || echo No process'
              bat 'pm2 start index.js'

            }
        }



        
    }
}
