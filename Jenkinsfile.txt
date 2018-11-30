pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                sh  """ go build main.go""" 
                  }
                       }
	
		     stage('Docker Build'){
                step{
                   sh  """ docker build	-t gotest . """
               }
                    }
   
         stage('push'){
               echo 'push'
          }		   
              
          }
      }
	  