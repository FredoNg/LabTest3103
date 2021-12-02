pipeline {
    agent { docker { image 'python:3.7.2' } }
    stages {
        stage('build') {
            steps {
                sh 'sudo pip install --upgrade pip'
                sh 'sudo pip install flask'
            }
        }
        stage('test') {
            steps {
                sh 'python test_feature.py'
            }
        }
    }
}