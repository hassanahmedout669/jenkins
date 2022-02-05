pipeline {
	// agent any
	agent {docker { image 'maven:3.6.3'}}
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"
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
