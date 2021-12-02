pipeline {
    agent { docker { image 'python:3.7.2' } }
    stages {
        stage('build') {
            steps {
                sh 'sudo chown -R "$USER":"$USER" ~/.local/lib'
				sh 'pip3 install --upgrade pip --user'
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