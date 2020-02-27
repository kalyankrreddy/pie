node {1

    stage('Checkout') {
        checkout scm
    }

	
    stage('Compile-Package') {
       
		def mvnHome = tool name: 'maven3', type: 'maven'
		//sh "${mvnHome}/bin/mvn package"
		sh """
			${mvnHome}/bin/mvn --version
			${mvnHome}/bin/mvn clean install
			"""
		
    }
}
