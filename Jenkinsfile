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
                echo 'building hello.go...'
                sh 'go build hello.go'
            }
         }
      
         stage("run") {
          
            steps {
                echo 'Running hello.go...'
                sh './hello'
            }
         }    
    }
}

