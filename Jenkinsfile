pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS616 first.cpp'
                build job: 'PES1UG20CS616-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS616'
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
