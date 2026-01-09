pipeline{
  agent {label 'node-1'}
  environment {
    DIR="job1"
    LOG_FILE="job-${env.BUILD_NUMBER}.log"
  }
  stages{
    stage("Build"){
      steps{
        sh "mkdir -p $DIR"
        sh "cd $DIR"
        sh "pwd"
        echo "Build-ID:${env.BUILD_ID}"        
        sh """
        echo "Build-NO:${env.BUILD_NUMBER}" > $LOG_FILE
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
