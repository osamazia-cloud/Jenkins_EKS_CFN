pipeline {
    agent any
    stages {
        stage('Deploy Stack') {
            steps {
            sh "$USER$"
            sh "aws cloudformation create-stack --stack-name EKS-Cluster --template-body file://EKS-Cluster.yml --region 'us-east-1'"
              }
             }
            }
            }
