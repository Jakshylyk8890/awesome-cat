pipeline {
    agent any
    environment {     
    DOCKERHUB_CREDENTIALS= credentials('dockerhubcredentials')     
} 
    stages {
        stage("build") {
            steps{
                sh 'sudo docker build -t user8890/jenkins-cat-frontend awesome_cats_frontend'
            }
        }
        stage("build2") {
            steps{
                sh 'sudo docker build -t user8890/jenkins-cat-backend awesome_cats_backend'
            }
        }
    }
}
