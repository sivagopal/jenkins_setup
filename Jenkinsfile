pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '/usr/local/bin/pip install --user -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }
      post {
        always {
	  junit 'tests/results/*.xml'
        }
      }    
    }
  }
}
