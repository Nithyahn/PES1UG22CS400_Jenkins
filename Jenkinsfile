pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/nithyahn/PES1UG22CS400_Jenkins.git'
            }
        }
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o hello'
            }
        }
        stage('Run') {
            steps {
                sh './hello'
            }
        }
    }
}
