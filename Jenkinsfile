pipeline {
    agent {
        docker {
            image 'node:10-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
		sh 'chown -R 111:113 "/.npm"'
                sh 'npm install' 
            }
        }
    }
}
