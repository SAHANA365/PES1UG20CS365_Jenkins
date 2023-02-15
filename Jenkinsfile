pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS365-1 hello_new.cpp'
                echo 'Build stage successful'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG20CS365-1'
                echo 'Test stage successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment successful'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

