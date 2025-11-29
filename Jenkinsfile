pipeline{
    stages{
        agent{
            docker{
                image amazon/aws-cli:latest
                reuseNode true
            }
        }
        stage("aws version"){
            sh'''
             aws --version

             '''
              
        }
    }
}