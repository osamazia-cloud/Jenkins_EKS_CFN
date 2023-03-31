pipeline {
    agent any
    stages {
        stage('Deploy Stack') {
            steps {
            sh "sudo apt-get install awscli"
            sh "aws cloudformation create-stack --stack-name EKS-Cluster --template-body file://EKS-Cluster.yml --region 'us-east-1'"
              }
             }
            }
            }
