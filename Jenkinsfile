pipeline {
    agent any

    stages {
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
