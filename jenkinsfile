pipeline{
  agent any
  stages{
     stage("Maven Build"){
       steps{
            sh "mvn clean package"
        }
     }
     stage('sonar_test') {
       environment {
         scannerHome = 'sonarscanner'
      }   
       steps{
           withSonarQubeEnv('sonarqube') { // If you have configured more than one global server connection, you can specify its name
           sh "${scannerHome}/bin/sonar-scanner -X"  
           }    
        }
     }
    } 
}            
