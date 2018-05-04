pipeline {
    agent {
        docker 'mhart/alpine-node:10'
    }

    stages {
        stage('Install') {
            steps {
                sh 'npm ci'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Publish') {
            environment {
                NPMRC = credentials('NPMRC')
            }
            steps {
                sh 'echo $NPMRC > .npmrc'
                sh 'npm publish'
            }
        }
    }
}