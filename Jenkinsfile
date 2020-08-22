pipeline {
   agent any
   environment {
    // environment variables and credential retrieval can be interspersed
    SOME_VAR = "SOME VALUE"
    // this assumes that "cred1" has been created on Jenkins Credentials
    CRED1 = credentials("cred1")
    INBETWEEN = "Something in between"
    // this assumes that "cred2" has been created in Jenkins Credentials
    CRED2 = credentials("cred2")
    // Env variables can refer to other variables as well
    OTHER_VAR = "${SOME_VAR}"
  }  
   stages{
	   	stage('Build'){
	   		steps{
	   			sh'echo "Hello World!"'
	   			sh'''
	   		  		echo "Multiline shell step works too" 
	   		  		echo "Un altra linea" 
	   		  		printenv
	   		  		ls -la 
	   			'''
	   		}
	   	}
   }
}