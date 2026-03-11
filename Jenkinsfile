pipeline{
   agent any

   environment {
    APP_NAME = 'frontend'
    TARGET_ENV = 'prod'
    URL = 'https://github.com/spoorthi2696/jenkins-pipeline.git'
    GIT_CREDS = 'spoorthi2696'
    CHECKOUT_BRANCH = 'main'
   }

     stages{
       stage ('Checkout'){
        git url: "${env.URL}",
            branch: "${env.BRANCH}",
            credentialsID: "${env.GIT_CREDS}"
       }

       } 
     
   stages{
      stage('shell syntax'){
      step{

        // Shell synatx
        sh '''
           echo $APP_NAME
           echo $TARGET_ENV
        '''
      }
    }
   }
}