pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
        sh "pwd"
        sh "mkdir -p job1"
        sh "cd job1"
        echo "Building version...${env.BUILD_NUMBER}"
        echo "Building version...${env.BUILD_NUMBER}" > job1-${env.BUILD_NUMBER}.log
      }
    }
    stage("Test"){
      steps{
        echo "Testing..."
      }    
    }
  }
}
