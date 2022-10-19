pipeline {
    agent any

    stages {
       stage('Source') {
            steps {
                echo "git pull reponame"
                cd dir
                ls *.xml | count
            }
        }
        stage('Build') {
            steps {
                echo 'Compile..'
            }
        }
       stage('Test') {
            agent {
                docker { image 'sonar cube' }
            }
            steps {
                sh 'running test'
            }
        }
        
        stage('integrationTest') {
            agent {
                docker { image 'amazon/aws-cli' }
            }
            steps {
                sh 'aws chechk server'
                sh 'aws deploy {SERVER_IP}'
            }
        }
    }
}

