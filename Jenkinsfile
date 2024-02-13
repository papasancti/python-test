pipeline {
  agent any
  stages {
    stage('Download') {
      steps {
        sh 'rm -rf *'
          script {
            try {
              dpkg-query -W python3 && dpkg-query -W flask
          } catch (e) {
              if ( ${e} == 1 ) {
                echo NOPE
              }
            } 
        }
      }
    }
  }
}
