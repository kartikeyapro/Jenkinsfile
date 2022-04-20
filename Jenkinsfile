pipeline {
    agent any

    tools {
      maven 'maven-3.8.5'
    }

    stages {
        stage('Git Clone') {
            steps {
              git credentialsId: 'github', url: 'https://github.com/kartikeyapro/ks.git'   
            }
			}
	
		    stage('Maven Clean') {
            steps {
			
			 sh 'mvn clean'
                
            }
			}
			
			stage('Maven Version') {
            steps {
              sh 'mvn --version'  
            }
			}
			
			stage('Maven Validate') {
            steps {
			
			 sh 'mvn validate'
                
            }
			}
			stage('Maven Compile') {
            steps {
               sh 'mvn compile'
            }
			}
			stage('Maven Package') {
            steps {
			   sh 'mvn package'
                
            }
            }
			
			stage('Maven Deploy') {
            steps {
			   sh 'mvn deploy'
                
            }
            }
        }
}

