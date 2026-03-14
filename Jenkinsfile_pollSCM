pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')
    }

    stages{
        stage('A') {
            steps {
                echo "This is a Stage to test poll SCM"
            }
        }

        stage('B') {
            steps {
                script {
                    try{
                        sh 'exit 1'
                    }catch(e) {
                        echo "caught the error: ${e}"
                    }finally {
                        echo "Disconnect it"
                    }
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