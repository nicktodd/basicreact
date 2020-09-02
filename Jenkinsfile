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
                sh 'aws s3 cp build/* s3://training.conygre.com/allstate/reactapp/* --region eu-west-1'
            }
        }
        
    }
}