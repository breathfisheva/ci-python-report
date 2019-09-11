stage('Python pytest Tests') {
	steps {
		sh 'pip install -r requirements.txt'
		sh 'pytest --junit-xml=test_results.xml test || true'
		junit keepLongStdio: true, allowEmptyResults: true, testResults: 'reports/report.xml'
	}
}