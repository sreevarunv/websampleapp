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
         
                   sh 'mvn package'
                 
              }
           }
           stage('Deploy to tomcat'){
               steps{
               deploy adapters: [tomcat7(credentialsId: '2a9f02d5-3d8b-4676-8f54-433ece81d019', path: '', url: 'http://13.233.115.29:8090/')], contextPath: null, onFailure: false, war: '**/*.war'
                }
           }
         }
       }
