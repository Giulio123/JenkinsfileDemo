pipeline {   
 environment{
 	P_STATUS = "NULL"
 }
  agent none

  stages {
    stage("Hello") {
      steps {
        echo "hello"
        // need to use script block to assign value
        script {
        	P_STATUS = currentBuild.result		
          currentBuild.result = "UNSTABLE"
        }
      }
    }
  }
  post {
    always { 
      echo "I ALWAYS run first and P_STATUS is $P_STATUS and currentBuild is $currentBuild.result"
    }
    unstable {
      echo "UNSTABLE runs after ALWAYS"
    }
  }
}