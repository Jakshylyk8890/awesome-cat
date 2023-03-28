pipeline {
    agent any
    environment {     
    DOCKERHUB_CREDENTIALS= credentials('dockerhubcredentials')     
} 
    stages {
        stage("build") {
            steps{
                sh 'sudo docker build -t user889090/jenkins-cat-frontend awesome_cats_frontend'
            }
        }
        
        stage("build2") {
            steps{
                sh 'sudo docker build -t user889090/jenkins-cat-backend awesome_cats_backend'
            }
        } 
        
        stage('Login to Docker Hub') {      	
          steps{                       	
	        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | sudo docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'                		
	        echo 'Login Completed'      
    }           
} 
        stage('Push frontend Image to Docker Hub') {         
         steps{                            
	     sh 'sudo docker push user889090/jenkins-cat-frontend'                 
             echo 'Push Image Completed'       
      }           
    }
        stage('Push backend Image to Docker Hub') {         
         steps{                            
	     sh 'sudo docker push user889090/jenkins-cat-backend'                 
             echo 'Push Image Completed'       
      }           
    }
    }
	emailext body: 'Test Message',
    subject: 'Test Subject',
    to: 'jakshylyk.ashyrmamatov@gmail.com
}
