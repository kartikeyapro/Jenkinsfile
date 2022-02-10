pipeline {
    agent any

    tools {
        maven "maven-3.0.5"
    }

    stages {
        stage('GitClone') {
            steps {
			git credentialsId: 'git_pass', url: 'https://github.com/kartikeyapro/ks.git'	 	
             
            } }
    stage('Maven Version') {
            steps {
			   sh 'mvn --version'               
            } }			

    stage('Maven Clean') {
            steps {
			sh 'mvn clean'      	
             
            } }
    stage('Maven Validate') {
            steps {
			sh 'mvn validate' 	
             
            } }		
    stage('SonarQube CodeScan'){
            steps {
            sh 'mvn sonar:sonar -Dsonar.host.url=http://104.154.92.41:9000 -Dsonar.login=ea5b0806baace67b284584c5639f6ff6e4b44ea4'    
            }
    }
    
    stage('Maven Compile') {
            steps {
			sh 'mvn compile' 	
             
            } }
    stage('Maven Test') {
            steps {
				
            sh 'mvn test'  
            } }	
    stage('Maven Package') {
            steps {
				
            sh 'mvn package'  
            } }
    stage('Maven Deploy') {
            steps {
			sh 'mvn deploy' 	
             
            } }					
    }
}			
  
