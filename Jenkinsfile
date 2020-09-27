pipeline {
    agent any
      stage('Deploy Cloudformation') {
		steps{
            try {
                 sh"/usr/local/bin/aws cloudformation create-stack --stack-name test-cicd-jenkins --template-body file://ec2.json  --region 'ap-south-1'"
            }
catch(err)
{'echo cloudformation creation failed'
        }
    }
}
}