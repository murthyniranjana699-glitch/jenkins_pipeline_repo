pipeline {
    agent any

    environment{
        DOCKER_USER = 'niranjan'
        AWS_ACCESS_KEY = '876740i0987987'

    }

    stages{
        stage('STAGE1'){

            environment{
                    STAGE = 'STAGE1'
                    }

            steps{
                echo "NAME: ${env.DOCKER_USER}"
                echo "AWS_ACCESS_KEY: ${env.AWS_ACCESS_KEY}"
                echo "STAGE: ${env.STAGE}"

                sh '''
                    env
                '''
            }

        } 

         stage('STAGE2'){

            environment{
                    STAGE = 'STAGE2'
                    }

            steps{
                echo "NAME: ${env.DOCKER_USER}"
                echo "AWS_ACCESS_KEY: ${env.AWS_ACCESS_KEY}"
                echo "STAGE: ${env.STAGE}"

                sh '''
                    env
                '''
            }

        } 
    }    
}