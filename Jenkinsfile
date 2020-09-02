pipeline {

    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'npm build'
            }
        }
        stage('Delivery') {
            steps {
                sh 'aws s3 cp --recursive build s3://react-test-nick --region eu-west-2'
            }
        }
        
    }
}