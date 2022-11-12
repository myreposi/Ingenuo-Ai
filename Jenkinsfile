pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --template-body=file://./ai-infra-stack_v1.yml --stack-name=vpc-infra"
              }
             }
            }
            }
