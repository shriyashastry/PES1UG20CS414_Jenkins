pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS414 PES1UG20CS414.cpp'
                build job: 'PES1UG20CS414-12'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS414'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
