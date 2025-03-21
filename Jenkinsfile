pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo ' Compiling C++ file...'
                    sh '''
                    g++ -o PES2UG22CS173-1 main/hello.cpp
                    '''
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo ' Running compiled program...'
                    sh '''
                    ./PES2UG22CS173-1
                    '''
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo ' Deploying Application...'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Check errors.'
        }
    }
}
