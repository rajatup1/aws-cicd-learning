pipeline{
    stages{
        stage("aws version"){
        agent{
            docker{
                image amazon/aws-cli:latest
                reuseNode true
            }
            sh'''
             aws --version

             '''
              
        }
    }
}
}