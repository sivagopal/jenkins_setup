node ('master'){
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/sivagopal/jenkins_setup.git'
   }
   stage('Build') {
      jrintMessage('Running pipeline')
      sh '/usr/local/bin/pip install -r requirements.txt'
      sh 'python test.py'
      printMessage('Pipeline Complete')
   }
}
def printMessage(message) {
    echo "${message}"
}
