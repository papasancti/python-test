pipeline {
  agent any
  
  stages {
    stage('Download') {
      steps {
        sh "rm -f *"
        script {
          set +e
          sh 'dpkg-query -W python3 flask'
          sh 'echo $?'
          set -e
         }
        sh 'mkdir app'
        sh 'wget https://raw.githubusercontent.com/papasancti/python-test/main/webpage.py?token=GHSAT0AAAAAACOEUWNHC2OEZD6BEGEFLCR4ZOLMHCA'
      }
    }
    
    stage ('TEST File') {
      input {
          message 'Contenuto cartella e applicativo mostrato. Procedere?'
      }
      steps {
        sh 'ls'
        sh 'cat webpage.py'
      }
    }
      
    stage ('TEST App') {
        input {
            message 'Applicativo lanciato. Attendo conferma URL per procedere.'
        }
        steps {
          sh 'python3 webpage.py'
        }
      }
      
    stage ('Done') {
        steps {
          echo 'Applicativo controllato e funzionante! :)'
      }
    }
  }
}
