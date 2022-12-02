pipeline{
  agent any
  stages{
    stage("Git Checkout"){
      steps{
            git credentialsId: 'github', url: 'https://github.com/Prasadfasi/GitHub-Actions.git'
           }
          }
     stage("Maven Build"){
       steps{
            sh "mvn clean package"
            sh "mv target/*.war target/mcs.war"
             }
            }
     stage("deploy-dev"){
       steps{
          sshagent(['tomcat-deplo']) {
          sh """
          scp -o StrictHostKeyChecking=no target/GitHub-Actions.war  
          ubuntu@yourip:/opt/tomcat/webapps/
          ssh ubuntu@yourip /opt/tomcat/bin/shutdown.sh
          ssh ubuntu@yourip /opt/tomcat/bin/startup.sh
           """
            }
          }
        }
      }
    }
