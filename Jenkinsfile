pipeline {
    agent any

    environment {
        REPO_URL = 'https://github.com/nithyahn/PES1UG22CS400_Jenkins.git'
        BRANCH = 'main'
        BINARY_NAME = 'hello'
        SOURCE_FILE = 'main/hello.cpp'  // <-- FIXED PATH
    }

    stages {
        stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }

        stage('Clone Repository') {
            steps {
                git branch: BRANCH, url: REPO_URL
            }
        }

        stage('Debug') {
            steps {
                echo "### Checking files in workspace ###"
                sh 'pwd'   // Print current directory
                sh 'ls -R' // List all files to verify hello.cpp exists
            }
        }

        stage('Compile') {
            steps {
                sh 'g++ -o ${BINARY_NAME} ${SOURCE_FILE}'
            }
        }

        stage('Run Executable') {
            steps {
                sh './${BINARY_NAME}'
            }
        }
    }

    post {
        success {
            echo "✅ Build and execution completed successfully!"
        }
        failure {
            echo "❌ Build failed! Check errors."
        }
    }
}
