node {

    stage('Checkout') {
        checkout scm
    }

	
    stage('Compile-Package') {
       
		def mvnHome = tool name: 'maven3', type: 'maven'
		sh "${mvnHome}/bin/mvn package"
		//mvn --version
		//mvn clean package
		//mvn clean install
		//
    }
}
