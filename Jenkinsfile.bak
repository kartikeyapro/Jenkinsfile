node {
    
    stage('Git Clone') {
 	   git credentialsId: 'git_pass', url: 'https://github.com/kartikeyapro/ks.git'	 
       }
   stage('mvn version') {
   	sh 'mvn --version'
   }
   stage('Maven Clean') {
		sh '''mvn clean'''       
    }
    stage('Maven Validate') {
		sh '''mvn validate''' 
    }
    stage('Maven Compile') {
		sh '''mvn compile'''  
    }
    stage('Maven Test') {
		sh '''mvn test''' 
    }
	stage('Maven Package') {
		sh '''mvn package''' 
    }
}

