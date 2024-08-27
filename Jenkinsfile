pipeline {
	agent any
	
	parameters {
  string defaultValue: 'DEV', name: 'ENVIRONMENT'
}



	stages {
	    stage('Checkout') {
	        steps {
			git 'https://github.com/samikshabokde14/siddhi.git'			       
		      }}
		stage('Build') {
	           steps {
			  sh 'mvn install'

	                 }}
		stage('Deployment'){
		    steps {
			script {
			 if ( env.ENVIRONMENT == 'QA' ){
        	sh 'cp target/siddhi.war /home/samiksha/Downloads/apache-tomcat-9.0.93/webapps'
                echo "deployment has been done on QA!"
			 }
			else if ( env.ENVIRONMENT == 'UAT' ){
    		sh 'cp target/siddhi.war /home/samiksha/Downloads/apache-tomcat-9.0.93/webapps'
                echo "deployment has been done on UAT!"
			
			}}}	
}}}


