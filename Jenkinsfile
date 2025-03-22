pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/nithyahn/PES1UG22CS400_Jenkins.git'  // Update with your repo URL
            }
        }
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o hello'  // Use correct path
            }
        }
        stage('Run') {
            steps {
                sh './hello'  // Execute compiled C++ program
            }
        }
    }
}
