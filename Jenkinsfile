//node {

    //stage('Checkout') {
    //    checkout scm
  //  }

node {
	stage('Checkout') {
        checkout scm
    }
    withMaven(mavenSettingsConfig: 'maven-settings-for-game-of-life', mavenInstallation: 'M3', jdk: 'Oracle JDK 8') {
      //  git 'https://github.com/cyrille-leclerc/my-spring-boot-app.git'
        sh "mvn clean package deploy"
    }
}	
	
//    def mvn_version = 'M2'
//withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
//   sh "mvn clean package"
// }
	
//    stage('pre-install') {
//       sh """
//		export MAVEN_HOME=/opt/apache-maven-3.6.0
//	export M2_HOME=/opt/apache-maven-3.6.0
//		export PATH=$PATH:$MAVEN_HOME:$M2_HOME/bin
//		mvn --version
//		mvn clean package
//		mvn clean install
//		"""
//   }
//}
