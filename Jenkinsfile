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
        stage('Bring Grid Down') {
            steps {
                    powershell " docker-compose down"
                    
                }
            }        
    }
}
