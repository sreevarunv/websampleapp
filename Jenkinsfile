pipeline{
    agent any
        stages{
            stage('compile stage'){
              steps{
                withMaven(maven:'maven'){
                   sh 'mvn clean compile'
                 }
              }
           }
           stage('testing stage'){
              steps{
                withMaven(maven:'maven'){
                   sh 'mvn test'
                 }
              }
           }
           stage('deploy stage'){
              steps{
                withMaven(maven:'maven'){
                   sh 'mvn deploy'
                 }
              }
           }
         }
       }
