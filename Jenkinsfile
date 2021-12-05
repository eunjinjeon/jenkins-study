pipeline {
  
    agent any
  
    stages {
      
        stage("build") {
          
            steps {
                echo 'building the application...'
            }
         }
      
         stage("test") {
          
           when {
              branch 'dev'
           }
           
            steps {
                echo 'testing the application...'
            }
         }
      
         stage("deploy") {
           
           when {
              branch 'main'
           }
          
            steps {
                echo 'deploying the application...'
            }
         }       
    }
  
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
      
      success {
            echo '**Success**'
      }
      
      failure {
            echo '**Failed**'
      }
    }

}

