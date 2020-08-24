pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
		sh 'chown -R 111:111 ~/.npm'
                sh 'npm install --unsafe-perm=true --allow-root' 
            }
        }
    }
}
