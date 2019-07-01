pipeline {
  agent any
  stages {
    stage('build') {
      steps {
	sh '/usr/local/bin/python -m venv env'
	sh 'source ./env/bin/activate'
        sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }   
    }
  }
}
