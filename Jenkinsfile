pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                sh  """ 
		       export PATH=$PATH:/goroot/bin:/gopath/bin
		       go build main.go """ 
                  }
        }
	
       stage('Docker Build'){
             steps{
                   sh  """ docker build	-t gotest . """
               }
        } 
       stage('push'){
            steps{
               withCredentials([UsernamePassword(credentialsId: 'sunil',usernameVariable: 'USER', passwordVariable: 'PASSWORD')]) {

         sh """
    docker login --username $USER -- password $PASSWORD
    docker push mygo 
        """
		      }
	     }
          }		   
              
          }
      }
	  
