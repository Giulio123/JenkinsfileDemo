 
pipeline {
  agent {
    dockerfile {
      /*
        * The Default is "Dockerfile" but this can be changed.
        * This will build a new container based on the contents of "Dockerfile.alternate"
        * and run the pipline inside this container
        */
      filename "Dockerfile.alternate"
 
    }
  }
  stages {
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'svn --version'
            }
        }
    }
}