pipeline {
   agent any  
   stages{
   	stage('Build'){
   		sh'echo "Hello World!"'
   		sh'''
   		  echo "Multiline shell step works too" 
   		  ls -lah 
   		'''
   	}
   }
}