pipeline {
    agent {
        docker 'node:10'
    }

    stages {
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Publish') {
            steps {
                sh 'echo $NPMRC > .npmrc'
                sh 'npm publish'
            }
        }
    }
}