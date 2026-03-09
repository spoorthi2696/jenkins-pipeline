pipeline {
    agent { label 'slave1'}

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
            steps {
                sh '''
                   sleep 3
                '''   
            }
        }
    }
}
