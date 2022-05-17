pipeline{	
	stages{
		stage("Fix the permission issue") {
            agent any
            steps {
                sh "sudo chown root:jenkins /run/docker.sock"
            }
        }
		stage('step 1'){
			steps{
				agent {
					docker {
						image 'openjdk:8-jdk-alpine'
					}
				}				
			}
		}
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