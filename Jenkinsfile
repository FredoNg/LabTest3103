pipeline {
    agent { docker { image 'python:3.7.2' } }
    stages {
        stage('build') {
            steps {
                sh 'pip install --upgrade pip --user'
                sh 'python3 -m pip install -r requirements.txt'
                sh 'pip install flask'
            }
        }
        stage('test') {
            steps {
                sh 'python test_feature.py'
            }
        }
    }
}