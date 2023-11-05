pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/briskdust/curriculum-app', branch: 'dev')
      }
    }

    stage('List Files') {
      parallel {
        stage('List Files') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Frontend Unit Test') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}