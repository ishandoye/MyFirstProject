#!groovy

pipeline {
    agent any

    environment {
        DEPLOY_HOST = '13.127.65.202'
        DEPLOY_DOC_ROOT = '/home/Project/'
        DEPLOY_USER = 'ishan.doye'
    }
    
    stages {
        stage('Deploy') {
            steps {
                
                sh "ssh -o StrictHostKeyChecking=no $DEPLOY_USER@$DEPLOY_HOST \"cd $DEPLOY_DOC_ROOT && git fetch origin && git reset --hard origin/master\""
            }
        }
    }
}  
