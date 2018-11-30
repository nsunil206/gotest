pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                sh  """ go build main.go""" 
                  }
                       }
		stages {
		     stage('Docker Build')
                step{
                   sh  """ docker build	-t gotest . """
               }
                    }
   stages {
         stage('push')
           echo 'push'
          }		   
              
          }
      }