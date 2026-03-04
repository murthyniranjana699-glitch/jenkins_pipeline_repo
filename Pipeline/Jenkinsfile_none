pipeline {
    agent any

    stages{
        stage('STAGE1'){
            steps{
                sh 'sleep 5'
                echo "This is the stage1"
                
            }

        } 
        stage('STAGE2'){
            steps{
                sh '''
                #!/bin/bash
                ls -lrt
                pwd
                sleep 10
                '''
                echo "This is the stage2"
            }
        }
            
    }
    
        
    
}
