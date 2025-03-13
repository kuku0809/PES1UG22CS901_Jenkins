pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                build 'PES1UG22CS901-1'
                sh 'g++ main/hell.cpp -o output'
                echo 'Build is complete'
            }
        }

        stage('Test') {
            steps {
                sh 'chmod +x output'
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
