pipeline {
    agent any

    stages{
        stage('STAGE1_A'){

            steps{
                catchError (buildResult: 'SUCCESS', stageResult: 'FAILURE'){
                    echo "This is Stage1_a running"
                    sh '''
                        sleep 10
                        exit 1
                    ''' }
                }
            }
             

        stage('STAGE1_B'){
            steps{
                Script{
                    try{
                        sh '''
                            sleep 5
                            exit 1 
                        '''
                    }
                    catch (err){
                        echo "Error Caught: $(err)"
                        currentBuild.result: 'SUCCESS'
                        currentBuild.result: 'FAILURE'

                    }
                }
            }

        }    
    }
}