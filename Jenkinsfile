pipeline {
    agent {
 label 'amazon-linux-slave'
}
    stages {
        stage('CreateDockerContainer') 
        { 
            steps {
              script{
		      sh ("""#!/bin/bash
                  "whoami"
		  "docker --version"
		 
		 "docker run -itd -p 90:80 nginx" 
		 """)
           }
            }
			  }
        stage('ViewRunningContainers') 
        { 
            steps {
                //
                        sh "docker ps -a"
                      }
        }
        stage('Verify') 
        { 
            steps {
                //
			sh "docker inspect"
            }
        }
    }
}
