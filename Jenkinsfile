pipeline {
    agent any
    stages {
        stage('Run Test') {
            steps {
                 powershell  "docker-compose up"
                }
        }
        stage('Bring Grid Down') {
            steps {
                    powershell " docker-compose down"
                    
                }
            }        
    }
}
