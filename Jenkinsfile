pipeline {
    agent any
      stages{

	      stage('Deploy Cloudformation') {
			steps{
                 			sh"/usr/local/bin/aws cloudformation create-stack --stackname test-cicd-jenkinss --template-body file://ec2.json  --region 'ap-south-1'"
            }    
}


}
}
