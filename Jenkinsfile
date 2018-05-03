pipeline {
    agent {
        dockerfile true
    }

    stages {
        stage('Build') {
            steps {
                echo 'Hello 11122'
                sh 'npm i'
                sh 'npm run build'
            }
        }
    }
}