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

    stage('Run test') {
      steps {
        sh 'npm run test'
      }
    }

    stage('Build') {
      steps {
        sh 'docker build -f jenkins-test/Dockerfile .'
      }
    }

  }
}