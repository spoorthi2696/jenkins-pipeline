pipeline{
   agent any

   environment {
    APP_NAME = 'frontend'
    TARGET_ENV = 'prod'
    GIT_URL = 'https://github.com/spoorthi2696/jenkins-pipeline.git'
    GIT_CREDS = 'spoorthi2696'
    CHECKOUT_BRANCH = 'main'
   }

     stages{
       stage ('Checkout'){
        steps{
        git url: "${env.GIT_URL}",
            branch: "${env.CHECKOUT_BRANCH}",
            credentialsId: "${env.GIT_CREDS}"
       }
       }
      stage ('shell syntax'){
      steps{

        // Shell synatx
        sh '''
           echo $APP_NAME
           echo $TARGET_ENV
        '''
      }
    }
   }
}  
