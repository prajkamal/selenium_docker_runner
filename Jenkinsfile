pipeline{
	agent any
	stages{
		stage("Turn on Grid"){
			steps{
				bat "docker-compose up"
			}
		}
		stage("Bring grid down"){
			steps{
				bat "docker-compose down"
			}
		}
	}
}
