pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/briskdust/curriculum-app', branch: 'dev')
      }
    }

    stage('List Files') {
      steps {
        sh 'ls -la'
      }
    }

  }
}