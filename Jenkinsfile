pipeline {
    agent any
    stages {
        stage('submit stack') {
            steps {  
                       sh "aws cloudformation create-stack --template-body=file://ai-infra-stack_v1.yml --region='us-east-2' --stack-name=ai-vpc-infra-stack"
                          sleep(time: 8, unit: 'MINUTES')
                          echo "Building basic stack"
                       sh "aws cloudformation create-stack --template-body=file://ai--vm-and-db-autoscal-stack.yml --region='us-east-2' --stack-name=Total-ai-vm-and-db-stack"
                          echo "Provisioning the whole stack of infra"
                }
            }
        }
    }

