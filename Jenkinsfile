pipeline {
    agent {
        dockerfile true
    }

    stages {
        stage('Build') {
            steps {
                echo 'Hello'
                sh 'npm i'
                sh 'npm run build'
            }
        }
    }
}