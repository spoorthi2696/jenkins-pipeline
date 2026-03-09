pipeline {
    agent any
    parameters { booleanParam(name: 'DEBUG_BUILD', defaultValue: true, description: '')
    choice(name: 'CHOICES', choices: ['one', 'two', 'three'], description: '')}

    stages{
        stage ('STAGE_1') {

            steps {
                sh '''
                   ls
                '''   
            }
        }
        stage ('STAGE_2') {

            steps {
                echo "STAGE 2"  
            }
        }
    }
}
