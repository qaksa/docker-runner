pipeline{
	agent any
	stages{
		stage("Starting the Grid Infrastructure"){
			steps{
				sh "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Executing TestCases"){
			steps{
				sh "docker-compose up telecom"
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: 'output/**'
			sh "docker-compose down"
		}
	}
	
}