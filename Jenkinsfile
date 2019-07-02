node ('master'){
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/sivagopal/jenkins_setup.git'
   }
   stage('Build') {
      printMessage('Running pipeline')
      sh '/usr/local/bin/pip install -r requirements.txt --user sivagopal'
      sh 'python test.py'
      printMessage('Pipeline Complete')
   }
}
def printMessage(message) {
    echo "${message}"
}
