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
        sleep 5
      }
    }
  }
  environment {
    env = 'ci'
    USER = 'pratik'
  }
}