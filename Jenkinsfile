node {

    stage('Checkout') {
        checkout scm
    }

	
    stage('pre-install') {
       sh """
		export MAVEN_HOME=/opt/apache-maven-3.6.0
		export M2_HOME=/opt/apache-maven-3.6.0
		export PATH=$PATH:$MAVEN_HOME:$M2_HOME:$HOME/bin
		mvn --version
		mvn clean package
		mvn clean install
		"""
   }
}
