pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    environment {
        FAVOURITE_FRUIT = 'Start testing by Lisa'
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'echo $FAVOURITE_FRUIT'
                withCredentials([string(credentialsId: 'datadogApiKey', variable: 'LISAKEY')]) {
                    sh 'echo $LISAKEY'
                }
            }
        }
    }
}
