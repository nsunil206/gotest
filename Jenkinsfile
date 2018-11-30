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
                step{
                   sh  """ docker build	-t gotest . """
               }
                    }
   
         stage('push'){
               echo 'push'
          }		   
              
          }
      }
	  
