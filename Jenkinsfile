pipeline {
	agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				echo "Path - $PATH"
				echo "Build Number - $env.BUILD_NUMBER"
				echo "BUILD ID - $env.BUILD_ID"
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
