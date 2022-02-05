pipeline {
	agent docker { image { node:14-alpine } }
	stages {
		stage('Build') {
			steps {
				sh 'docker -v'
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
