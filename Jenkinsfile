pipeline {
    agent any
      stages{

	      stage('Deploy Cloudformation') {
			steps{
            		try {
                 			sh"/usr/local/bin/awscloudformation create-stack --stackname test-cicd-jenkins --template-body file://ec2.json  --region 'ap-south-1'"
            }
catch(err)
{'echo cloudformation creation failed'
        }
    }
}
}
}