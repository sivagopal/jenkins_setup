pipeline {
  agent any
  stages {
    stage('build') {
      steps {
	    pip install -r requirements.txt
      }
    }
    stage('test') {
      steps {
	    ./test.py 
      }   
    }
  }
}
