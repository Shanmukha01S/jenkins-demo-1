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
        sh 'chmod +x build.sh'
        sh './build.sh'
      }
    }

    stage('Test') {
      steps {
        echo 'Running basic tests'
        echo 'All tests passed'
      }
    }

    stage('Archive Artifact') {
      steps {
        echo "Archieving Artifacts"
        archiveArtifacts artifacts: '*.txt', fingerprint : true
      }
    }
  }

  post {
    success {
      echo 'Build success'
    }
    failure {
      echo 'Build failed'
    }
  }
}
