pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Build"
				echo '$PATH'
				echo 'Build Number - $env.BUILD_NUMBER'
				echo '$env.BUILD_ID'
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integrate') {
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
