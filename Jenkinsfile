pipeline {
   
    agent any
    stages {
        stage('Run Test') {
            steps {
                //sh
                bat "docker-compose up"
            }
        }
        stage('Bring grid down') {
            steps {
                //sh
                bat "docker-compose down"
            }
        }
      }
}