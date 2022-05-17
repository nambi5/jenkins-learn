pipeline{
	agent {
		docker {
			image 'node:16.13.1-alpine'
		}
	}
	stages{
		stage('Build'){
			steps{
				// sh 'node --version'
				echo 'Build'				
			}
		}
		stage('Test'){
			steps{
				echo 'Test'
			}
		}
		stage('Integration Test'){
			steps{
				echo 'Integration Test'
			}
		}
	}
	post{
		always {
			echo "All good"
		}
		success {
			echo "pipeline success"
		}
		failure {
			echo "pipeline crash"
		}
	}
}