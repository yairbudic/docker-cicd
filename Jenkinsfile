pipeline {
    agent any
    stages {
        stage('Pre-build') {
            steps {
                sh 'DOCKER_BUILDKIT=1 docker build --target pre-build .'
            }
        }
        stage('build') {
            steps {
                sh 'DOCKER_BUILDKIT=1 docker build --target build .'
            }
        }
        stage('test') {
            steps {
                sh 'DOCKER_BUILDKIT=1 docker build --target test .'
            }
        }
        stage('security') {
            steps {
                sh 'DOCKER_BUILDKIT=1 docker build --target security .'
            }
        }
        stage('backend') {
            steps {
                sh 'DOCKER_BUILDKIT=1 docker build --target back-end .'
            }
        }
        stage('front-end') {
            steps {
                sh 'DOCKER_BUILDKIT=1 docker build --target front-end .'
            }
        }
        stage('deploy') {
            steps {
                sh 'DOCKER_BUILDKIT=1 docker build --target deploy .'
            }
        }
        stage('post') {
            steps {
                sh 'DOCKER_BUILDKIT=1 docker build --target post .'
            }
        }
    }
}

      
