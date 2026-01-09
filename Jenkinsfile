pipeline{
  agent any
  environment {
    DIR="job-${env.BUILD_NUMBER}"
  }
  stages{
    stage("Build"){
      steps{
        sh "pwd"
        sh "mkdir -p $DIR"
        sh "cd $DIR"
        sh """
        echo "Building version...${env.BUILD_NUMBER}" > log${env.BUILD_NUMBER}
        """
      }
    }
    stage("Test"){
      steps{
        echo "Testing..."
      }    
    }
  }
}
