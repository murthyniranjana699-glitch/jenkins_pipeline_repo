pipeline {
    agent any

    parameters {
        booleanParam(name: 'DEPLOY', defaultValue: false, description: 'Deploy to production')
    }

    environment {
        CURRENT_ENV = 'prod'
    }

    stages {

        stage('STAGE1 when branch') {
            when {
                branch 'main'
            }
            steps {
                echo 'This stage is running'
                sh '''
                    sleep 10
                '''
            }
        }

        stage('CHECKOUT') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                        credentialsId: 'aws_pem',
                        url: 'https://github.com/murthyniranjana699-glitch/jenkins_pipeline_repo.git'
                    ]]
                ])
            }
        }

        stage('Deploy Stage') {
            when {
                expression { params.DEPLOY }
            }
            steps {
                echo 'This is the final stage running'
                sh 'sleep 10'
            }
        }
    }
}