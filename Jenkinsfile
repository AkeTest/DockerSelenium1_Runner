pipeline {
    agent any
    stages {
		stage('Pull lastest images') {
            steps {
                 powershell  "docker pull vonsdpcker/selenium-docker"
                }
        }
        stage('Start Grid') {
            steps {
                 powershell  "docker-compose up -d hub chrome firefox"
                }
        }
        stage('Run Test') {
            steps {
                 powershell  "docker-compose up search-moduleF book-moduleC"
                }
        }
               
        }
    post{
        always{
            archiveArtifacts artifacts: 'output/**'
            powershell " docker-compose down"
            }

        }
    }
