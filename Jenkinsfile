pipeline {
    agent any
    stages {
        stage('submit stack') {
            steps {  
                timeout(time: 30, unit: 'MINUTES'){
                     sh "aws cloudformation create-stack --template-body=file://ai-infra-stack_v1.yml --region='us-east-2' --stack-name=ai-vpc-infra-stack"
                }
                     {
                    sh "aws cloudformation create-stack --template-body=file://ai--vm-and-db-autoscal-stack.yml --region='us-east-2' --stack-name=Total-ai-vm-and-db-stack"
                }
            }
        }
    }
}
