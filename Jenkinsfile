pipeline {
    agent { label 'slave2'}

    stages{
        stage ('STAGE_1') {
            steps {
                sh '''
                   ls -lrt
                   pwd
                   env
                   sleep 2
                '''   
            }
        }
        stage ('STAGE_2') {
            agent any
            steps {
                sh '''
                   sleep 3
                '''   
            }
        }
    }
}
