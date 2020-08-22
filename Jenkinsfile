pipeline {
   agent any
   
   stages{
	   	stage('Build'){
	   		steps{
	   			sh'echo "Hello World!"'
	   			sh''' 
	   		  		echo "Un altra linea" 
	   		  		printenv
	   		  		ls -la 
	   			'''
	   		}
	   	}
   }
}