pipeline {
    agent any
    
    parameters {
        choice(name: 'GIT_URL', choices: [
        'https://github.com/spoorthi2696/Test1.git',
        'https://github.com/spoorthi2696/DevSecOps-Microdegree.git'
        ])
        
        choice(name: 'SERVER', choices: ['test','staging','PROD']) 
    }

    environment {
        CHECKOUT_BRANCH = 'main'
        GIT_CREDS = 'spoorthi2696'
    }

    stages {

        stage('Checkout') {
            steps {
                git url: "${params.GIT_URL}",
                    branch: "${env.CHECKOUT_BRANCH}",
                    credentialsId: "${env.GIT_CREDS}"
            }
        }

        stage('Shell Syntax') {
            steps {
                sh '''
                   echo $CHECKOUT_BRANCH
                   echo $SERVER
                '''
            }
        }

    }
}