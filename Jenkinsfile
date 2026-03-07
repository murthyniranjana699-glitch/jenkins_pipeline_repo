pipeline {
    agent any

    stages{
        stage('STAGE1'){

            steps{
                echo "This the Stage 1 is running"

                sh '''
                    sleep 10
                '''
            }

        } 

        stage('PARALLEL STAGE'){
            parallel{
                stage{
                    steps{
                        echo "Windows Testing"

                        sh '''
                           sleep 10
                        '''
                    }

                } 

                stage{
                    steps{
                        echo "MACOS Testing"

                        sh '''
                           sleep 10
                        '''
                    }

                } 
            }  
        }    
    }

    stages{
        stage('STAGE1'){

            steps{
                echo "This the final stage is running"

                sh '''
                    sleep 10
                '''
            }   
        }  

    }   
}