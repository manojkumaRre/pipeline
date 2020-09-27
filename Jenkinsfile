pipeline {
    agent any
    stages{
        stage('install git') {
        try{
         sh 'sudo yum install git -y'
        }
        catch(err)
        {
         sh"echo git installation failed"
        }
        }
        stage('git clone') {
        try{
        sh 'git clone https://github.com/manojkumaRre/pipeline.git'
        }
        catch(err)
        {
          sh"Repo is not cloned"
        }
        }
        stage('Deploy Cloudformation') {
            try {
                 sh"aws cloudformation create-stack --stack-name "test-cicd-jenkins" --template-body file://ec2.json  --region 'ap-south-1'"
            }
            catch(err)
            {
                sh"Cloudformation creation failed"
            }
        }
    }
}
