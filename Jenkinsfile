node {

    stage('Checkout') {
        checkout scm
    }

    stage('Build'){
        sh "mvn clean install"
    }

    stage('Artifact'){
        sh """
		mkdir workbench
		#cd target
		zip -r workbench/my-app-1.0-SNAPSHOT.jar.zip target/my-app-1.0-SNAPSHOT.jar
		"""
    }

    stage('dev deploy'){
	sh "cd ansible && export ANSIBLE_HOST_KEY_CHECKING=False && ansible-playbook -i inventory playbook.yml"
    }

}
