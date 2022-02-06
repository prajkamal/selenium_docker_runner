pipeline{
	agent any
	stages{
		stage("Turn on Grid"){
			steps{
				bat "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Execute Tests"){
			steps{
				bat "docker-compose up selenium-tests"
			}
		}
		stage("Bring grid down"){
			steps{
				bat "docker-compose down"
			}
		}
	}
}
