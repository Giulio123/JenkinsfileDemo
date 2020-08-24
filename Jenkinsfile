pipeline {   
 
  agent none

  stages {
    stage("Hello") {
    	environment{
        	VAV = currentBuild.result
        }
      steps {
        echo "hello"
        
        // need to use script block to assign value
        script {
        	if(VAV!=null)
        	 echo " VAV is $VAV"	
          currentBuild.result = "UNSTABLE"
        }
      }
    }
  }
  post {
    always { 
      echo "I ALWAYS run first"     
  	}
    unstable {
      echo "UNSTABLE runs after ALWAYS"
    }
  }
}