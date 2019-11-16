pipeline{
    agent any
    
    tools{
        maven 'maven'
    }
        stages{
            stage('compile stage'){
              steps{
                
                   sh 'mvn clean compile'
                 
              }
           }
           stage('testing stage'){
              steps{
                    echo "mvn package from maven"
                   sh 'mvn package'
                 
              }
           }
           stage('copying warfile'){
               steps{
                   echo "deploying to tomcat"
               sh 'sudo cp /var/lib/jenkins/workspace/Pipeline-jenkinsfile-mvn-compile-test-deploy/target/SampleWebapp.war /opt/tomcat/webapps/'
                }
              }
         }
       }
