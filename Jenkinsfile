node {

    stage('Git Clone') { 
     git credentialsId: 'github', url: 'https://github.com/kartikeyapro/ks.git'
    }
    
    stage('Maven Clean') { 
      sh 'mvn clean'
    }
	
	stage ('Maven Version')
	{
		sh 'mvn --version'
	}
	
	stage('Maven Validate') { 
      sh 'mvn validate'
    }
	
	stage('Maven Compile') { 
      sh 'mvn compile'
    }
	
	stage ('SonarScan'){
	  sh 'mvn sonar:sonar -Dsonar.host.url=http://34.70.92.117:9000 -Dsonar.login=f2c6e63720f9ed8b3143569d3b9046cb3fd16e80'
	 
	}
	
	stage('Maven Test') { 
      sh 'mvn test'
    }
	
	stage('Maven Package') { 
      sh 'mvn package'
    }
	
}	

    
