pipeline {
    agent any

    stages {
        stage('Checkout'){
          steps{
            git branch: 'main', credentialsId: 'spoorthi2696', url: 'https://github.com/spoorthi2696/Test1.git'
          }
        }

        stage('Check code quality repo1'){
            steps{
                sh '''
                   pwd
                   ls -lrt

                '''
            }

        }
        stage('Checkout2'){
            steps{
                checkout scmGit(branches: [[name: '*/main']],  
                userRemoteConfigs: [[
                    credentialsId: 'spoorthi2696', 
                    url: 'https://github.com/spoorthi2696/DevSecOps-Microdegree.git'
                ]]
                ) 
            }
        }

        stage('Check code quality repo2'){
            steps{
                sh '''
                   pwd
                   ls -lrt

                '''
            }

        }
    }
}
    