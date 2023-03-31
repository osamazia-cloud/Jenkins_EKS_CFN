@Library('github.com/releaseworks/jenkinslib') _
pipeline {
    agent any
    stages {
        stage('Deploy Stack') {
            steps {
             withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
                AWS("--region=eu-west-1 s3 ls")
            }
             sh "pwd"
            // sh 'aws --version'
            //sh "aws cloudformation create-stack --stack-name EKS-Cluster --template-body file://EKS-Cluster.yml --region 'us-east-1'"
              }
             }
            }
            }
