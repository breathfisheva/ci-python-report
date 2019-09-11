pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build') {
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh '. /tmp/venv/bin/activate && python -m pytest --junitxml=reports/report2.xml'
      }
      post {
        always {
          junit 'reports/*.xml'
        }
      }
    }
  }
}