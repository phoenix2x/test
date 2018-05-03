pipeline {
    agent {
        docker 'node:9.11.1'
    }

    stages {
        stage('Install') {
            steps {
                sh 'npm i'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}