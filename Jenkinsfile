pipeline{
  agent any
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
        sh """
        echo "Build:${env.BUILD_NUMBER}" > $LOG_FILE
        """
      }
    }
    stage("Test"){
      steps{
        echo "Testing..."
      }    
    }
  }
        
    post {
        always {
            cleanWs()
        }
    }
  
}
