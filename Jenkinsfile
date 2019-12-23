pipeline {
    agent {
 label 'amazon-linux-slave'
}
    stages {
        stage('CreateDockerContainer') 
        { 
            steps {
              
                   sh "whoami"
		  sh "docker --version"
		  sh "docker rm -f"
		 sh "docker run -itd -p 90:80 nginx" 
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
			sh "docker container inspect nginx"
            }
        }
    }
}
