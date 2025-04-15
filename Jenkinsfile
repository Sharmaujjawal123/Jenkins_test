pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo 'Repo Cloned Successfully!'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                bat 'dir' // For Windows
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests... (pretend)'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying... (pretend)'
            }
        }
    }
}
