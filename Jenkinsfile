pipeline {
    agent any 
    stages {
        stage( 'Build') {
            steps {
                sh("make")
                echo 'Build Stage Successful'
            }
        }
        stage ('Test' ) {
            steps {
                sh("./hello_world")
                echo 'Test Stage Successful' 
            }
            
        }
        stage( 'Deploy') {
            steps {
                echo 'Deployment successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}