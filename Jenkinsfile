pipeline {
    agent any
    stages {
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
