pipeline{
  agent any
  stages{
    
    stage("init"){
      steps{
          echo 'init application...'
      }
    }
    
    
     stage("build"){
      steps{
          echo 'build application...'
      }
    }
    
     stage("test"){
       when{
         branch 'dev'
       }
       
      steps{
          echo 'test application...'
      }
    }
  }
  
  post {
    always{
     echo 'always' 
    }
    success{
     echo 'success' 
    }
    failure{
     echo 'failure' 
    }
    
  }
  
}
