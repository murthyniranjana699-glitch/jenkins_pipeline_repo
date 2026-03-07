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
                stage('Windows Testing'){
                    steps{
                        echo "This is Windows Testing running"

                        sh '''
                           sleep 10
                        '''
                    }

                }

                stage('MACOS Testing'){
                    steps{
                        echo "This is MACOS Testing running"

                        sh '''
                           sleep 10
                        '''
                    }

                } 
            }  
        }    

   
        stage('STAGE3'){

            steps{
                echo "This the final stage is running"

                sh '''
                    sleep 10
                '''
            }   
        }  

    }
}