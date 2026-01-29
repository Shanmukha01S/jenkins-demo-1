pipeline {
  agent any
  stages{
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
    failure {
      echo 'Build failed'
    }
  }
}
