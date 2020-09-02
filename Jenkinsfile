pipeline {

    agent any
    
    stages {
        stage('Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run-script build'
            }
        }
        stage('Delivery') {
            steps {
                sh 'aws s3 cp --recursive build s3://react-test-nick --region eu-west-2'
            }
        }
        
    }
}