pipeline {
    agent any
    stages {
        stage("aws version"){
        agent{
            docker{
                image 'amazon/aws-cli:latest'
                args '--entrypoint=""'
                reuseNode true
            }
        }

            steps {
                withCredentials([usernamePassword(credentialsId: 'aws-creds', passwordVariable: 'AWS_SECRET_ACCESS_KEY', usernameVariable: 'AWS_ACCESS_KEY_ID')]) {
                    sh'''
                    aws --version
                    aws s3 ls
                    
                    '''
                 }
                
            }
              
        }
    }
}