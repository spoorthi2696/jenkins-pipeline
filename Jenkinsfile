pipeline {
    agent any

    stages {
        stage('Checkout'){
          steps{
            git branch: 'main', credentialsId: 'spoorthi2696', url: 'https://github.com/spoorthi2696/Test1.git'
          }
        }
        stage('parallel stages'){
             parallel{
             stage('Check code quality repo1'){
             steps{
                sh '''
                   pwd
                   ls -lrt
                   sleep 10
                '''
                }

              }
             stage('Build')
             steps{
              sh '''
                pwd
                ls -lrt
                sleep 10
              '''  
            }
         }
      }
    }
    
    }


    