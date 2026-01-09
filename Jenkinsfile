pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
        echo "Building version...${env.BUILD_NUMBER}"
        sh "touch job1-${env.BUILD_NUMBER}.log"
      }
    }
    stage("Test"){
      steps{
        echo "Testing..."
      }    
    }
  }
}
