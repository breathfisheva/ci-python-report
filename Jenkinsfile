stage('Python pytest Tests') {
	dir('python/pytest') {
		sh 'pip install -r requirements.txt'
		sh 'pytest --junit-xml=test_results.xml test || true'
		junit keepLongStdio: true, allowEmptyResults: true, testResults: 'reports/report.xml'
	}
}