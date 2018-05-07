pipeline {
    agent {
        dockerfile true
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
            when {
                allOf {
                    environment name: 'CHANGE_ID', value: ''
                    branch 'master'
                }
            }
            steps {
                sh 'echo $NPMRC > .npmrc'
                sh 'npm publish'
            }
        }
    }
}