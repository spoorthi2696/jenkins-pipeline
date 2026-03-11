pipeline {
    agent any

    stages {

        stage('Checkout') {
            environment {
                 APP_NAME = 'frontend'
                 TARGET_ENV = 'prod'
                 GIT_URL = 'https://github.com/spoorthi2696/jenkins-pipeline.git'
                 GIT_CREDS = 'spoorthi2696'
                 CHECKOUT_BRANCH = 'main'
    }
            steps {
                git url: "${env.GIT_URL}",
                    branch: "${env.CHECKOUT_BRANCH}",
                    credentialsId: "${env.GIT_CREDS}"
            }
        }

        stage('Shell Syntax') {
            steps {
                sh '''
                   echo $APP_NAME
                   echo $TARGET_ENV
                '''
            }
        }

    }
}