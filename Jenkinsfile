pipeline{
   agent any
   stages{
	stage('clean workspace')
	{
           steps{
              sh ' rm -r *'
	      sh ' rm -r ../../../../www/html/*'
	   }
	}

        stage('git scm clone'){
             
	     steps{
                  
		  sh ' git clone https://github.com/Chandrikatck/aws-codepipeline-s3-codedeploy-linux.git -b master '

	     }
 
	}
	stage('deploy'){
              steps{
                sh 'mv aws-codepipeline-s3-codedeploy-linux/* ../../../../www/html'
	      }
	}
     
   }
  
}
