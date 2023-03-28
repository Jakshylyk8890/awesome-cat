pipeline {
    agent any
    stages {
        stage("test") {
            steps{
                sh 'docker build -t user8890/jenkins-cat-frontend awesome-cats_frontend'
            }
        }
    }
}
