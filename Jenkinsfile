pipeline {
    
    agent any
    
    stages {
        
        stage("build") {
          
            steps {
                echo 'building the application...'
            }
        }

        stage("check") {

            when{
                branch 'example'
            }
          
            steps {
                echo 'checking the application...'
            }
        }

        stage("test") {
          
            steps {
                echo 'testing the application...'
            }
        }

        stage("dev") {

            when {
                branch 'dev'
            }

            environment {
                ACCESS_KEY = credentials('gittest')
            }
          
            steps {
                echo 'developing the application...'
                echo "build id = ${BUILD_ID}"
                echo "access key id = ${ACCESS_KEY_USR}"
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
