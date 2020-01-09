pipeline {
    agent any
  stages {
    stage('test') {
      steps {
        sh """pip install unittest-xml-reporting
              python test_calc.py"""
      }   
    }
  }