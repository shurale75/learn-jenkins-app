pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Hello2') {
            steps {
                sh '''
                        echo "Hello World"
                        whoami
                    '''
            }
        }
        stage('without Docker') {
            steps {
                sh 'echo "Without DOCKER"'
            }
        }
        stage('with Docker') {
            agent {
                docker {
                    image 'node:18-alpine' 
                    reuseNode: true
                }
            }
            steps {
                sh 'echo "With DOCKER"'
            }
        }
    }
}
