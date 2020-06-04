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
                   sh 'pip3 install pytest --user'
            }
        } 
       stage('test') {
            steps {
		sh 'python3 -m pytest'
            }
        }
stage('deploy') {
            steps {
		sh 'ansible-playbook -i ip-server setup.yml'
            }
        }  
  }
}
