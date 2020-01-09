pipeline {
    agent any
  stages {
    stage('test') {
      steps {
        sh """
		pip install unittest-xml-reporting
              python test_calc.py"""
         }
	  post {
        always {
			junit keepLongStdio: true, testResults: 'results.xml'
			publishHTML target: [
				reportDir: '/var/lib/jenkins/workspace/unit-test-pipeline/',
				reportFiles: 'index.html',
				reportName: 'Coverage Report - Unit Test'
			]	
      }   
    }
  }
  }
  }