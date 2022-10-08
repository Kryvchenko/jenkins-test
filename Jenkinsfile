pipeline {
  agent any
  tools {nodejs "18.10.0"}
  stages {
    stage('preflight') {
      steps {
        script {
            if (isUnix()) {
                 sh 'node -v'
            } else {
                bat 'node -v'
            }
        }
      }
    }
    //  stage('cash clean') {
    //   steps {
    //     script {
    //         if (isUnix()) {
    //              sh 'npm cache verify'
    //         } else {
    //             bat 'npm cache verify'
    //         }
    //     }
    //   }
    // }
    stage('build') {
      steps {
        script {
        if (isUnix()) {
                 sh 'npm install'
            } else {
                bat 'npm install'
            }
        }
      }
    }
    stage('test') {
      steps {
        script {
        if (isUnix()) {
                 sh 'npm run test'
            } else {
                bat 'npm run test'
            }
       }
      }
    }
  }
}