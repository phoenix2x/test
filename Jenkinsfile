pipeline {
    agent {
        dockerfile true
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