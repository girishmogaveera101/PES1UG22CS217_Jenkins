pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                script {
                    sh 'git clone https://github.com/gaganchandan-bot/PES1UG22CS205_Jenkins.git'
                }
            }
        }
        
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o pes1ug22cs205-1 PES1UG22CS205_Jenkins/pes1ug22cs205.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './pes1ug22cs205-1'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'deploy'
                // Add deployment steps here
            }
        }
    }
    
    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
