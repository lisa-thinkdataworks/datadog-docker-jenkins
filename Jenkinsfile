pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    environment {
        APIKEY = credentials('datadogApiKey')
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'echo APIKEY'
                sh 'echo $APIKEY'
            }
        }
    }
}
