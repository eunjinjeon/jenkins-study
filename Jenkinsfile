pipeline {
  
    agent any

     tools {
        go 'go1.16.9'
    }
    environment {
        GO111MODULE = 'on'
    }
  
    stages {
      
        stage("build") {
          
            steps {
                echo 'building the application...'
            }
         }
      
         stage("test") {
          
            steps {
                echo 'testing the application...'
            }
         }
      
         stage("deploy") {
          
            steps {
                echo 'deploying the application...'
            }
         }       
    }
}

