pipeline {
    agent any
    environment {
        CURRENT_ENV = 'prod'
    }

    stages {

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

        stage('STAGE1 when branch') {
            steps {
                echo 'This stage is running'
                sh '''
                    sleep 10
                '''
            }
        }

    }
}