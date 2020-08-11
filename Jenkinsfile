pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    stages {
        stage('Test') {
            steps {
		withCredentials([string(credentialsId: 'datadogApiKey', variable: 'DATADOG_API_KEY')]) {
                    sh 'env' 
		}
            }
        }
    }
}

