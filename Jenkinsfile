pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Use the full path to pip
                sh '/opt/anaconda3/bin/pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                // Use the full path to python
                sh '/opt/anaconda3/bin/python -m unittest test_app.py'
            }
        }
        stage('Deploy') {
            steps {
                // Use the full path to python
                sh '/opt/anaconda3/bin/python app.py'
            }
        }
    }
}
