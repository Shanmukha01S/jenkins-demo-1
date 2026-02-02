pipeline {
  agent any

  stages {

    stage('Checkout') {
      steps {
        checkout scm
        echo 'Code checked out from GitHub'
      }
    }

    stage('Build') {
      steps {
        echo 'Build stage started'
        sh 'ls -l'
      }
    }

    stage('Test') {
      steps {
        echo 'Running tests'
        echo 'All tests passed'
      }
    }

    stage('Archive') {
      steps {
        sh 'echo "Build successful" > build.txt'
        archiveArtifacts artifacts: 'build.txt'
      }
    }
  }

  post {
    success {
      echo 'Pipeline executed successfully'
    }
    failure {
      echo 'Pipeline failed'
    }
  }
}
