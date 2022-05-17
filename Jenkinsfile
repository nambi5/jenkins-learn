pipeline{
	agent any
	stages{
		stage('Build'){
			steps{
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
			echo "pipeline crash"
		}
		failure {
			echo "pipeline crash"
		}
	}
}