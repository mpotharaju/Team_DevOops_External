pipeline {
  
  agent any
  
  environment {
      port = 8080
  }

  
  stages {

    stage("Setting env variables"){
        steps{
                echo 'Retrieving source from github' 
                git branch: 'master',
                url: 'https://github.com/kenkool23/Team_Dev_Oops_External.git/'
                echo 'Did we get the source?' 
                sh 'ls -a'
            }
          }
    

    stage("Build Docker image"){
        steps{
                echo 'Building Docker image' 
                sh 'gcloud builds submit -t gcr.io/mar-roidtc307/devoops_external:latest .'
                echo 'Done' 
            }
          }
    }

  }
