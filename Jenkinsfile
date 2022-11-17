pipeline {
    agent any
    stages {
        stage('submit stack') {
            steps {
                     sh "aws cloudformation create-stack --template-body=file://infra-stack.yml --region='us-east-2' --stack-name=ai-vpc-infra-stack"
                     timeout(time: 10, unit: 'MINUTES') {
                    sh "aws cloudformation create-stack --template-body=file://ai-vm-and-db-autoscal-stack.yml --region='us-east-2' --stack-name=Total-ai-vm-and-db-stack"
                }
            }
        }
    }
}
