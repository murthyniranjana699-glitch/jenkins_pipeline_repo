pipeline {
    agent any

    environment{
        DOCKER_USER = 'niranjan'
        AWS_ACCESS_KEY = '876740i0987987'

    }

    stages{
        stage('STAGE1'){
            steps{
                echo "NAME: ${DOCKER_USER}"
                echo "AWS_ACCESS_KEY: ${AWS_ACCESS_KEY}"

                sh '''
                    env
                '''
            }

        } 
    }
    
}