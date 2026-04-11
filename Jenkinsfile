pipeline {
    agent any

    stages {

        stage('Build docker image') {
            steps {
                sh 'docker build -t ahmedgamil/docker-react -f Dockerfile.dev .'
            }
        }

        stage('Run tests') {
            steps {
                sh 'docker run -e CI=true ahmedgamil/docker-react npm run test'
            }
        }

    }
}