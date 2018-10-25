pipeline {
  agent any
  stages {
    stage('Kickoff') {
      parallel {
        stage('Kickoff') {
          steps {
            sh 'echo "I am $USER"'
            sh 'touch FileA'
            fileExists 'FileA'
          }
        }
        stage('Parallel_kickoff') {
          steps {
            echo 'This is parallel Job'
          }
        }
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