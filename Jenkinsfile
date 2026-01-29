pipeline {
  agent any
  stages{
    stage('checkout'){
      steps {
        git 'https://github.com/Shanmukha01S/jenkins-demo-1.git'
      }
    }
    stage('Build'){
      steps{
        sh 'echo "Building stage"'
        sh './build.sh'
      }
    }
  }
  post {
    success{
      echo 'Build success'
    }
    Failure {
      echo 'Build failed'
    }
  }
}
