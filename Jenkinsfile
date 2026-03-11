pipeline {
    agent any
    parameters{
        booleanParam (name: 'DEPLOY', description: 'when to deploy to production')
    }
    environment{
        CURRENT_ENV=   'prod'
    }

    stages{
        stage('STAGE1 when branch'){
            when {
                branch 'main'
            }
            steps{
                echo 'This is stage is running'
                    sh '''
                        sleep 10
                        exit 1
                    ''' 
            }
        }
             
        stage('STAGE2 when enviroment'){
            when {   
              environment name: 'CURRENT_ENV', value: 'prod'    
            }
            steps{
                echo 'This is stage 2 running for environment'
                sh 'sleep 15'
            }

        }   

        stage('when parameter'){
            when{
                expression {params.DEPLOY == false}
            }
            steps{
                echo 'This is the Final stage runnig'
                sh 'sleep 10'
            }
        } 
    }
}