pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    environment {
        FAVOURITE_FRUIT = credentials['datadogApiKey']
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'echo $FAVOURITE_FRUIT'
            }
        }
    }
}
