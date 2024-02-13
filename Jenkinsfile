pipeline {
  agent any
  stages {
    stage('Download') {
      steps {
        sh 'rm -rf *'
        sh 'dpkg-query -W python32 && dpkg-query -W flask'
        sh 'export STAT=$(echo $?)'
        if ( $STAT == 1) {
          sh 'echo "NOPE"'
        }
      }
    }
  }
}
