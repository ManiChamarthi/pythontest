pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage("Approval"){
    input { 
      message "To Suspend Wiz Users click on OK"
      ok "Approve"
    }
      steps {
        echo "executing"
        sh "python3 --version"
      }
  }
    stage('hello') {
      steps {
        sh 'python -m pip install pandas'
        sh 'python3 mytest.py'
      }
    }
  }
}
