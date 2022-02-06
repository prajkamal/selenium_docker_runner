pipeline{
	agent any
	stages{
		stage("Pull Latest Image"){
			steps{
				bat "docker pull prajkamal/seleniumtests"
			}

		}
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
	/*
	post{
		always{
			archiveArtifacts artifacts: 'output/* *'
		}
	}
	*/
}
