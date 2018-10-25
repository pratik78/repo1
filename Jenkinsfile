pipeline {
  agent any
  stages {
    stage('Kickoff') {
      steps {
        sh 'echo "This is kickoff"'
      }
    }
  }
  environment {
    myagent = 'agent1'
  }
}