pipeline{
	agent {
		docker {
			image 'openjdk:8-jdk-alpine'
		}
	}
	stages{
		stage('Build'){
			steps{
				sh 'java --version'
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