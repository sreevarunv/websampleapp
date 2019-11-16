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
               sh 'cp **/*.war /opt/tomcat/webapps/'
                }
              }
         }
       }
