pipeline{
    agent any
    stages {
        stage("aws version"){
        agent{
            docker{
                image 'amazon/aws-cli:latest'
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