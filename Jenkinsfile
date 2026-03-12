pipeline {
    agent any

    stages{
        stage('A') {
            steps {
                echo "This is a Stage"
            }
        }

        stage('B') {
            steps {
                catchError(stageResult: 'SUCCESS', buildResult: 'SUCCESS'){
                    Sh 'exit 1'
                }
            }
        }

        stage('C') {
            steps{
                echo "Continue to the next stages"
            }
        }
    }
}