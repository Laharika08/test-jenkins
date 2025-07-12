pipeline {
   agent any

   stages{
     stage('checkout'){
       steps{
          git branch: 'main', url: 'https://github.com/Laharika08/test-jenkins/tree/main' 
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
