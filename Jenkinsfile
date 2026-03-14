pipeline {

    agent any

    triggers{
        cron('H/5 * * * *')
    }

    options{
        ansiColor('xterm') 
        disableConcurrentBuilds(abortPrevious: true)
        buildDiscarder(logRotator(numToKeepStr: '2'))
        disableResume()
        timeout(time: 2, unit: 'MINUTES')
    }

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