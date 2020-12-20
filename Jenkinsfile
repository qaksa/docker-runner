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
		stage("Bringing down the Infrastructure")
		{
			steps{
				sh "docker-compose down"
			}
		}
	}
}