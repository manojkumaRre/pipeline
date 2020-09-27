pipeline {
    agent any
    stages{
        stage('Deploy Cloudformation') {
            steps {
                script
                { 
                    sh " export AWS_DEFAULT_REGION=ap-south-1"
                    sh " aws cloudformation create-stack --stack-name test-cicd-jenkins --template-body file://ec2.json  --region 'ap-south-1' "}
            }

        }
    }
}
