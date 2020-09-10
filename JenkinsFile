pipeline{
   agent any

  stages{

       stage('Compile Stage'){

               steps{
           
                withMaven(maven : 'maven_3_7'){
                   sh 'mvn clean compile'
            }
         }
     }
 
      stages{

       stage('Testing Stage'){

               steps{
           
                withMaven(maven : 'maven_3_7'){
                   sh 'mvn test'
            }
         }
     }

    stage('Deploying Stage'){

               steps{
           
                withMaven(maven : 'maven_3_7'){
                   sh 'mvn deploy'
            }
         }
     }
  }
