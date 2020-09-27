pipeline {
    agent any
    stages{
        stage('Deploy Cloudformation') {
            steps {
                script
                { sh " aws cloudformation create-stack --stack-name "test-cicd-jenkins" --template-body file://ec2.json  --region 'ap-south-1' "}
            }

        }
    }
}
