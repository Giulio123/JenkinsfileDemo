pipeline {
  agent {
    dockerfile true
  }
  stages {
    stage("foo") {
      steps {
        sh 'cat /hi-there'
        sh 'echo "The answer is 42"'
      }
    }
  }
}