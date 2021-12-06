pipeline {
  
    agent any
  
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
  
    stages {
      
        stage("build") {
          
          environment {
            AN_ACCESS_KEY = credentials('gittest') 
          }
          
            steps {
              echo 'building the application...'
              echo "name is ${params.PERSON}"
              echo "text is ${params.BIOGRAPHY}"
              echo "booleanParam is ${params.TOGGLE}"
              echo "choice is ${params.CHOICE}"
              echo "password is ${params.PASSWORD}"
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

