pipeline {
    agent any
    stages{
        stage('install git') 
steps{
        try{
         sh'sudo yum install git -y'
        }
        catch(err)
        {
         sh'echo git installation failed'
        }
        }
}
stage('git clone') {
 
steps{
        try{
        sh'git clone https://github.com/manojkumaRre/pipeline.git'
        }
        catch(err)
        {
          'Repo is not cloned'
        }
        }
}
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