pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/nithyahn/YPES1UG22CS400_Jenkins.git'  // Update with your repo URL
            }
        }
        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o hello'  // Compile C++ file
            }
        }
        stage('Run') {
            steps {
                sh './hello'  // Execute compiled C++ program
            }
        }
    }
}
