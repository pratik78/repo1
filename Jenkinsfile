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
        git(url: 'git@github.com:pratik78/test.git', branch: 'master')
      }
    }
  }
  environment {
    env = 'ci'
    user = 'pratik'
  }
}