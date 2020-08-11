pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    stages {
        stage('Test') {
            steps {
		withCredentials([string(credentialsId: 'datadogApiKey', variable: 'datadogApiKey')]) {
                    sh 'echo $datadogApiKey'
                    sh 'env |grep datadogApiKey'
		}
            }
        }
    }
}

