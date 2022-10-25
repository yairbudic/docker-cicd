pipeline {
    agent any

    stages {
        stage('Pre-build stg') {
            steps {
                echo 'Prebuild actions..'
            }
        }
        stage('Build') {
            steps {
              sh 'echo "docker build --target Build"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "docker build --target test"'
            }
        }
        stage('Security') {
            steps {
                sh 'echo "docker build --target security""'
            }
        }
        stage('Back-end') {
            steps {
                sh 'echo "docker build --target backend""'
            }
        }
        stage('Front-end') {
            steps {
                sh 'docker build --target Front-end'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "docker build --target deploy"'
            }
        }
        stage('Post') {
            steps {
                echo "Clear env"
            }
        }
    }
}
