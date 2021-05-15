pipeline {
	agent any
	tools {
    	maven 'local-maven'
	}
	stages {
    		stage("Checkout") {   
        		steps {               	 
            			git branch: 'main', url: 'https://github.com/trinichacon/project-spring-io'
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
		stage("Package") {          	 
        		steps {  	 
            		sh "mvn package"          	 
	       		}
		}
	}
}
