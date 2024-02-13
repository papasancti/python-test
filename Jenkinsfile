pipeline {
  agent any
  stages {
    stage('Download') {
      steps {
        sh 'rm -rf *'
        sh 'dpkg-query -W python3 && dpkg-query -W flask'
        sh 'export STAT=$(echo $?)'
        script {
          if ( $STAT == 1) {
            sh 'echo "NOPE"'
          }
        }
      }
    }
  }
}
