pipeline {
    agent { docker { image 'python:3.7.2' } }
    stages {
        stage('build') {
            steps {
				sh 'sudo chmod 777 /usr/local/bin/pip'
                sh 'pip install --upgrade pip'
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