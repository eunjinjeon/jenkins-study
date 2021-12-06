pipeline {
    
    agent any
    
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

    post {
        always {
            echo 'I will always post'
        }
        success {
            echo 'Success...!'
        }
        failure {
            echo 'Failed...T.T'
        }
    }
}
