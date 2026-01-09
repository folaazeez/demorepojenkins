pipeline{
  agent {label 'node-1'}
  environment {
    DIR="job1"
    LOG_FILE="job-${env.BUILD_NUMBER}.log"
  }
  parameters{
    string(name: 'PERSON', defaultValue: 'Fola', description: 'what should I call you?')
  }
  stages{
    stage("Build"){
      environment {
        DIR2="job1000"
      }      
      steps{
        echo "Hello ${params.PERSON}"
        sh "mkdir -p $DIR"
        sh "cd $DIR"
        sh "pwd"
        echo "DIR2:$DIR2"
        echo "Build-ID-env:${env.BUILD_ID}"
        echo "Build-ID:$BUILD_ID"                
        echo "Build-NUMBER:$BUILD_NUMBER"                
        sh """
        echo "Build-NO-env:${env.BUILD_NUMBER}" > $LOG_FILE
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
