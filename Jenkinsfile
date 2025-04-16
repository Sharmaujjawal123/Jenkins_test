pipeline {
    agent any

    stages {
        stage('pull code from github') {
            steps {
                git url 'https://github.com/Sharmaujjawal123/Jenkins_test.git', branch:'main'
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
                bat 'start  cmd /c "node index.js"'
            }
        }



        // stage('Deploy') {
        //     steps {
        //         echo 'Deploying... (pretend)'
        //     }
        // }
    }
}
