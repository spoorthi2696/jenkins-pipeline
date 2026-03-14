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
                script {
                    try{
                        sh echo 'hi'
                    }catch(e) {
                        echo "caught the error: ${e}"
                    }finally {
                        echo "Disconnect"
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