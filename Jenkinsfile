pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
		withCredentials([string(credentialsId: 'datadogApiKey', variable: 'datadogApiKey')]) {
                    sh 'echo $datadogApiKey'
		}
            }
        }
    }
}
