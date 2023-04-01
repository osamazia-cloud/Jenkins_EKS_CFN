pipeline {
    agent any
    parameters {
        string(name: "KeyPairName", defaultValue: "KeyPair", trim: true, description: "Name of an existing EC2 key pair (for SSH-access to the worker node instances)")
    }
    stages {
        stage('Deploy Stack') {
            steps {
             sh "pwd"
             sh 'aws --version'
             sh "aws cloudformation create-stack --stack-name EKS-Cluster --template-body file://EKS-Cluster.yml --region 'us-east-1' --parameters ParameterKey=KeyPairName,ParameterValue=KeyPair"
              }
             }
            }
            }

// @Library('github.com/releaseworks/jenkinslib') _
// pipeline {
//     agent any
//     parameters {
//         string(name: "KeyPairName", defaultValue: "KeyPair", trim: true, description: "Name of an existing EC2 key pair (for SSH-access to the worker node instances)")
//         string(name: "WorkerNodesInstanceType", defaultValue: "t2.medium", trim: true, description: "EC2 instance type for the worker nodes")
//         string(name: "NumWorkerNodes", defaultValue: "2", trim: true, description: "Number of worker nodes to create")
//     }
//     stages {
//         stage('configure aws profile'){
//             steps{
//                 withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
//                     AWS("--region=us-east-1 s3 ls")
//                 }
//             }
//         }
//         stage('Deploy Stack') {
//             steps {
//                 script{
//              sh "pwd"
//              sh 'aws --version'
//              sh "aws cloudformation create-stack --stack-name EKS-Cluster --template-body file://EKS-Cluster.yml --region 'us-east-1' --parameters ParameterKey=KeyPairName,ParameterValue="${params.KeyPairName}" ParameterKey=WorkerNodesInstanceType,ParameterValue="${params.WorkerNodesInstanceType}" ParameterKey=NumWorkerNodes,ParameterValue="${params.NumWorkerNodes}""
//               }
//             }
//              }
//             }
//             }
