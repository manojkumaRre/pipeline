pipeline {
    agent any
      stages{

	      stage('Deploy Cloudformation') {
			steps{

                 	sh"/usr/local/bin/aws cloudformation create-stack --stack-name test-cicd-jenkins --template-body file://ec2.json --parameters file://ec2.param.json --region 'ap-south-1'"

                 			
            }    
}


}
}
