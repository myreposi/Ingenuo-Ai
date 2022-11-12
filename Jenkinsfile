pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --template-body=file://ai--vm-and-db-stack.yml --stack-name=Total-ai2-vm-and-db-stack"
              }
             }
            }
            }
