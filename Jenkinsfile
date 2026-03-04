pipeline {
    agent none

    parameters{
        string(name: 'NAME', default: 'defaultValue', description: 'Please provide info about you')
        booleanParam(name: 'SKIP_TEST', default: 'false', description: 'test failes hence failed')
        choice(name: 'BRANCH', choices:['master', 'staging', 'prod'] description: 'choose the proper env for deployment')
    }

    stages{
        stage('STAGE1'){

            agent {label 'my_slave1'}

            steps{
                echo "TNAME: ${params.NAME}"
                echo "SKIP_TEST: ${params.SKIP_TEST}"
                echo "BARNCH TO DEPLOY: ${params.BRANCH}"
            }

        } 
    }
    
}
