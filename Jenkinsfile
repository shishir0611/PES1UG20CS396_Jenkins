pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o task5_output task5.cpp'
                build job: 'PES1UG20CS396-1'
            }
        }
        stage('Test') {
            steps {
                sh './task5_output > output.txt'
                sh 'cat output.txt'
            }
        }
        stage('Deploy') {
            steps {
                echoes 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
