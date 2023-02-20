pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building..."
                sh '''
                python3 helloworld.py
                echo "-------------------------------------1"
                cd myapp
                pip3 install fire
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing..."
                sh '''
                cd myapp
                python3 hello.py
                python3 hello.py --name=Brady
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver...'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
