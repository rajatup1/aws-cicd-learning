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
          environment{
            AWS_BUCKET_NAME = 'deno-s3-bucket '
          }

          steps {
                withCredentials([usernamePassword(credentialsId: 'aws-creds', passwordVariable: 'AWS_SECRET_ACCESS_KEY', usernameVariable: 'AWS_ACCESS_KEY_ID')]) {
                    sh'''
                    aws --version
                    echo "Hello S3!" > index.html
                    aws s3 cp index.html s3://$deno-s3-bucket/index.html
                    
                    '''
                 }
                
            }
              
        }
    }
}