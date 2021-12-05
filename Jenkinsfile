pipeline {
  
    agent any

     tools {
        go 'go-1.16.9'
    }
    environment {
        GO111MODULE = 'on'
    }
  
    stages {
      
        stage("build") {
          
            steps {
                echo 'building the application...'
                sh 'go build hello.go'
            }
         }
      
         stage("test") {
          
            steps {
                echo 'testing the application...'
                sh './hello'
            }
         }
      
         stage("deploy") {
          
            steps {
                echo 'deploying the application...'
            }
         }       
    }
}

