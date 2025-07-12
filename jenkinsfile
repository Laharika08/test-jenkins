pipeline {
   agent any

   stages{
     stage('checkout'){
       steps{
          git 'https://github.com/Laharika08/test-jenkins/tree/main', branch:'main' 
       }
     }
     stage('Install Dependencies'){
       steps{
        bat 'npm install'
       }
     }
     stage('Run Tests'){
       steps{
         bat 'npm test'
       }
     }
     stage('Deploy'){
       steps{
         echo 'deploying the application'
       }
     } 
   }
 post{
   success{
      echo'pipeline completed successfully!'
   }
   failure{
      echo'pipeline failed'
   }
 }
}
