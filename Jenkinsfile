
pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				eho "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	}
	
	post {
		always {
			echo 'I will run in any condition.'
		}
		success{
			echo 'I will run if pipeline get success'
		}
		failure{
			echo 'I will run when pipeline get fail'
		}
	}
}
