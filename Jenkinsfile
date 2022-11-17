pipeline {
    agent any
    stages {
        stage('submit stack') {
            steps {  
                       sh "aws cloudformation create-stack --template-body=file://ai-infra-stack_v1.yml --region='us-east-2' --stack-name=ai-vpc-infra-stack"
                          sleep(time: 15, unit: 'MINUTES')
                       sh "aws cloudformation create-stack --template-body=file://ai--vm-and-db-autoscal-stack.yml --region='us-east-2' --stack-name=Total-ai-vm-and-db-stack"
                }
            }
        }
    }
}
