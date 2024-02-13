pipeline {
  agent any
  stages {
    stage('Download') {
      steps {
        sh 'rm -rf *'
        script {
          sh 'set +e'
          sh 'dpkg-query -W python3 && dpkg-query -W flask'
          sh 'STAT=$(echo $?)'
          sh """
            if [ $STAT -eq 1 ]
            then
              echo NOPE
            fi
          """
          sh 'set -e'
        }
      }
    }
  }
}
