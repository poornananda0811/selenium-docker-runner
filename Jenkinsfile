pipeline {
   
    agent any
    stages {
        //stage('Run Test') {

        stage('pull latest image')  {
        steps {
        bat "docker pull poornanandatangirala0811/selenium-docker"
        }
        }
        stage('start grid') {
            steps {
                //sh
                //bat "docker-compose up"
                bat "docker-compose up -d hub chrome firefox"
            }
        }
        //stage('Bring grid down') {
         stage('Run test') {
            steps {
                //sh
               // bat "docker-compose down"
                bat "docker-compose up search-module1"
            }
        }
    }
    post{
        always{
                 archiveArtifacts artifacts: 'output/**'
                 bat "docker-compose down"
                }
        }
    }
       // stage('stop grid') {
          //          steps {
                        //sh
                       // bat "docker-compose down"
             //           bat "docker-compose down"
            //        }
