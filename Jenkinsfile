pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/Kryvchenko/jenkins-test', branch: 'master')
      }
    }

    stage('Install ') {
      steps {
        sh 'npm install'
      }
    }

  }
}