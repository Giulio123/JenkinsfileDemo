pipeline { 
	environment {
	// environment variables and credential retrieval can be interspersed
	SOME_VAR = "SOME VALUE"
	// this assumes that "cred1" has been created on Jenkins Credentials
	CRED1 = credentials("6fb13357-a6d1-4a5b-aac9-c9cbf3f0d76f")
	INBETWEEN = "Something in between"
	// this assumes that "cred2" has been created in Jenkins Credentials
		CRED2 = credentials("0d34d8e1-b771-4660-b98d-263ca47b5e94")
	// Env variables can refer to other variables as well
	OTHER_VAR = "${SOME_VAR}"
	}
  	agent any  
	stages{
		stage('Build'){
			steps{
				// environment variables are not masked
				sh 'echo "SOME_VAR is $SOME_VAR"'
				sh 'echo "INBETWEEN is $INBETWEEN"'
				sh 'echo "OTHER_VAR is $OTHER_VAR"'

				// credential variables will be masked in console log but not in archived file
				sh 'echo $CRED1 > cred1.txt'
				sh 'echo $CRED2 > cred2.txt'
				//archive "**/*.txt" IS DEPRECATED 
				archiveArtifacts artifacts: '**/*.txt'   
			}
		}
	}
}