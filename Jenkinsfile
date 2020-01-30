pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                bat 'SET'
                bat 'git rev-parse --abbrev-ref HEAD'
            }
        }
    }
}