pipeline {
    agent none

    stages{
        stage ('STAGE_1') {

            agent { label 'slave1'}

            steps {
                sh '''
                   ls -lrt
                   pwd
                   env
                   sleep 10
                '''   
            }
        }
        stage ('STAGE_2') {

            agent { label 'slave2'}

            steps {
                sh '''
                   sleep 3
                '''   
            }
        }
    }
}
