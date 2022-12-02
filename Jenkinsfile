pipeline{
  agent any
  stages{
     stage("Maven Build"){
       steps{
            sh "mvn clean package -X"
            //sh "mv target/*.war target/mcs.war"
             }
            }
     //stage("deploy-dev"){
       //steps{
          //sshagent(['tomcat-deplo']) {
          //sh """
          //scp -o StrictHostKeyChecking=no target/GitHub-Actions.war  
          //ubuntu@yourip:/opt/tomcat/webapps/
          //ssh ubuntu@yourip /opt/tomcat/bin/shutdown.sh
          //ssh ubuntu@yourip /opt/tomcat/bin/startup.sh
           //"""
           // }
          //}
        //}
      }
    }
