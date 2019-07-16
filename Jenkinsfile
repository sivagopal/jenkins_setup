pipeline {
  agent any 
  stages {
    stage('build') {
      steps {
        sh '/usr/bin/pip install --user -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }
    }
  }
}
