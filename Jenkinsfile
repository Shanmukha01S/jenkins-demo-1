pipeline {
  agent any
  
  stages{
    
    stage('checkout'){
      steps{
        echo 'code checked out from guthub'
      }
    }
    stage('Build'){
      steps{
        echo 'Build stage started'
        sh 'ls -l'
      }
    }
    stage('Test'){
      steps{
        echo 'Runnig tests'
        echo 'All test passed'
      }
    }
    stage('Archieve'){
      steps{
        sh 'echo "Build successfull" > build.txt'
        archieveArtifacts artifacts: 'build.txt'
      }
    }
  }
post{
  success{
    echo 'pipeline executed successfully'
  }
  failure{
    echo 'pipeline failed'
  }
}
}

  


        
    
