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
    }
}
