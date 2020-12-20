pipeline{
	agent any
	stages{
		stage("Starting the Executions"){
			steps{
				sh "docker-compose up"
			}
		}
		stage("Bringing down the Grid Environment")
		{
			steps{
				sh "docker-compose down"
			}
		}
	}
}