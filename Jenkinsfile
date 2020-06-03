pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'python3 -m py_compile main.py'
            }
        }
	stage('install pytest') {
             steps {
                   sh 'pip install pystest --user'
            }
        } 
       stage('test') {
            steps {
		sh 'python3 -m pytest'
            }
        }
    }
}
