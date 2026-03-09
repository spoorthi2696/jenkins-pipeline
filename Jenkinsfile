pipeline {
    agent any

    stages{
        stage ('STAGE_1') {
            steps {
                sh '''
                   ls -lrt
                   pwd
                   env
                   sleep 5
                '''   
            }
        }
        stage ('STAGE_2') {
            steps {
                sh '''
                   sleep 3
                '''   
            }
        }
    }
}
