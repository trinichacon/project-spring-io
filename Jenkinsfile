pipeline {
	agent any
	tools {
    	maven 'local-maven'
	}
	stages {
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
		stage("Package") {          	 
        		steps {  	 
            		sh "xmvn package"          	 
	       		}
		}
	}
}
