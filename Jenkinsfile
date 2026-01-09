pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
        echo "Build..."
        echo "cma-${env.BUILD_NUMBER}"
      }
    }
    stage("Test"){
      steps{
        echo "Testing..."
      }    
    }
  }
}
