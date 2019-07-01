pipeline {
  agent any
  stages {
    stage('build') {
      steps {
	sh 'PATH=$WORKSPACE/venv/bin:/usr/local/bin:$PATH'
	sh 'virtualenv env'
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
