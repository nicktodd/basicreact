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
                sh 'aws s3 cp build/* s3://training.conygre.com/allstate/reactapp/* --region eu-west-1'
            }
        }
        
    }
}