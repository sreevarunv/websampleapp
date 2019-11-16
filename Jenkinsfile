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
         
                   sh 'mvn test'
                 
              }
           }
          
         }
       }
