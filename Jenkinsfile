pipeline {
  stages {
    stage('Download') {
      steps {
        sh "rm -rf *"
        if ( ! sh "dpkg-query -W python32 && dpkg-query -W flask") {
          sh "apt install -y python3 flask"
        }
        sh "mkdir app"
      }
    }
  }
}
