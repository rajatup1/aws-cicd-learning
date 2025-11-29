pipeline{
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

            steps{
                sh'''
                aws --version

                '''
            }
              
        }
    }
}