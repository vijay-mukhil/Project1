pipeline {
    agent any

    stages {
        stage('Source Code') {
            steps {
                echo 'Building..'
                git "https://github.com/vijay-mukhil/Project1.git"
                
            }
        }
        stage('Install Dependencies') {
            steps {
                echo 'Testing..'
                sh npm install
            }
        }
        stage('Build Docker Image') {
            steps {
                echo 'Deploying....'
                gcloud builds submit --tag 
            }
        }
        stage('Update Deployment') {
            steps {
                echo 'Deploying....'
                gcloud container clusters get-credentials cluster-1 --zone us-central1-c --project may2021dtc501
                kubectl set image deployment
            }
        }
    }
}
