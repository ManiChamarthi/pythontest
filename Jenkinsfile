pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage('hello') {
      steps {
        sh 'pip install pandas'
        sh 'python3 mytest.py'
      }
    }
  }
}