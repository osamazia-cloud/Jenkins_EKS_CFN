pipeline {
    agent any
    parameters {
        string(name: "Key_Pair", defaultValue: "KeyPair", trim: true, description: "Name of an existing EC2 key pair (for SSH-access to the worker node instances)")
        string(name: "InstanceType", defaultValue: "t2.medium", trim: true, description: "EC2 instance type for the worker nodes")
        string(name: "NumberOfWorkerNodes", defaultValue: "2", trim: true, description: "Number of worker nodes to create")
    }
    stages {
        stage('Deploy Stack') {
            steps {
             sh "pwd"
             sh 'aws --version'
             sh "aws cloudformation create-stack --stack-name EKS-Cluster --template-body file://EKS-Cluster.yml --region 'us-east-1' --parameters ParameterKey=Key_Pair,ParameterValue="${params.Key_Pair}" ParameterKey=InstanceType,ParameterValue="${params.InstanceType}" ParameterKey=NumberOfWorkerNodes,ParameterValue="${params.NumberOfWorkerNodes}""
              }
             }
            }
            }
