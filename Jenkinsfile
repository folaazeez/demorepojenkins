pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
        sh "mkdir job1"
        sh "pwd"
        sh "cd job1"
        echo "Building version...${env.BUILD_NUMBER}"
        echo "Building version...${env.BUILD_NUMBER}" > "touch job1-${env.BUILD_NUMBER}.log" 
      }
    }
    stage("Test"){
      steps{
        echo "Testing..."
      }    
    }
  }
}
