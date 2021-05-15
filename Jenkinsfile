pipeline {
	agent any
	tools {
    	maven 'local-mvn'
	}
	stages {
		stage("Checkout") {   
			steps {               	 
			git url: 'https://github.com/rpabo/spring-project-demo.git'          	 

			}    
		}
		stage('Build') {
			steps {
			sh "mvn compile"  	 
			}
		}

		stage("Unit test") {          	 
			steps {  	 
			sh "mvn test"          	 
			}
		}

		stage("Package Artifact") {          	 
			steps {  	 
			sh "mvn package"          	 
			}
		}
	}
}
