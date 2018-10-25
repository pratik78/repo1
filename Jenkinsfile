pipeline {
  agent any
  stages {
    stage('Kickoff') {
      steps {
        sh 'echo "I am $USER"'
      }
    }
    stage('Build') {
      steps {
        git(url: 'git@github.com:pratik78/test.git', branch: 'master', credentialsId: 'pratik78')
      }
    }
  }
  environment {
    env = 'ci'
    user = 'pratik'
  }
}