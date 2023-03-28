pipeline {
    agent any
    stages {
        stage("test") {
            steps{
                sh 'sudo docker build -t user8890/jenkins-cat-frontend awesome_cats_frontend'
            }
        }
    }
}
