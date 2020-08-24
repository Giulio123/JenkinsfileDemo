pipeline {   
 
  agent none

  stages {
    stage("Hello") {
      steps {
        echo "hello"
        environment{
        	VV = currentBuild.result
        }
        // need to use script block to assign value
        script {
        	if(VV!=null)
        	 echo " VV is $VV"	
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