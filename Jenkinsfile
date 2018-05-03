pipeline {
    agent {
        docker 'node:9.11.1'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Hello 111'
                sh 'npm i'
                sh 'npm run build'
            }
        }
    }
}