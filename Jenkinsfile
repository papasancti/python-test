pipeline {
  agent any
  
  stages {
    stage('Download') {
      steps {
        sh 'rm -rf *'
        sh 'mkdir app'
        sh 'cd app && curl http://raw.githubusercontent.com/papasancti/python-test/main/webpage.py?token=GHSAT0AAAAAACOEUWNHC2OEZD6BEGEFLCR4ZOLMHCA'
      }
    }
    
    stage ('TEST File') {
      input {
          message 'Contenuto cartella e applicativo mostrato. Procedere?'
      }
      steps {
        sh 'ls'
        sh 'cat app/webpage.py'
      }
    }
      
    stage ('TEST App') {
        input {
            message 'Applicativo lanciato. Attendo conferma URL per procedere.'
        }
        steps {
          sh 'python3 app/webpage.py'
        }
      }
      
    stage ('Done') {
        steps {
          echo 'Applicativo controllato e funzionante! :)'
      }
    }
  }
}
