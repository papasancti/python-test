pipeline {
  agent any
  stages {
    stage('Download') {
      steps {
        sh 'rm -rf *'
          script {
            try {
              sh 'dpkg-query -W python3 && dpkg-query -W flask'
          } catch (e) {
              sh 'echo NOPE'
            }
          }
      }
    }
  }
}
