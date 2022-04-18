node {

    stage('Git Clone') { 
     git credentialsId: 'github', url: 'https://github.com/kartikeyapro/ks.git'
    }
    
    stage('Maven Clean') { 
      powershell 'mvn clean'
    }
	
	stage('Maven Validate') { 
      powershell 'mvn validate'
    }
	
	stage('Maven Compile') { 
      powershell 'mvn compile'
    }
	
	stage('Maven Test') { 
      powershell 'mvn test'
    }
	
	stage('Maven Package') { 
      powershell 'mvn package'
    }
	
}	

    
