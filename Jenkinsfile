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
	
		
	stage('Maven Test') { 
      sh 'mvn test'
    }
	
	stage('Maven Package') { 
      sh 'mvn package'
    }
	stage('Release to aws') {
    
            withAWS(region:'us-east-1', credentials:'ksstore'){
                s3Upload(bucket:"ksstore", workingDir:'target', target/*.war'); // pick your jar or whatever you need
            
        }
	
}	

    
