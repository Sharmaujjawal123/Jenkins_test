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
                bat 'taskkill /F /IM node.exe || echo Node not running'
                 bat 'start "" cmd /c "node index.js" & exit 0'
            }
        }



        
    }
}
