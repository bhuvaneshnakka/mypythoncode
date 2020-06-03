pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'python3 -m py_compile main.py'
            }
        }
	stage('test') {
            steps {
		sh 'python3 -m pytest'
            }
        }
    }
}
