pipeline {
	agent any 
	parameters {
		choice(name: 'ENVIRONMENT', choices: ['QA','UAT'], description: 'Pick Environment value')
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/sejal/Documents/devops-software/apache-tomcat-9.0.85/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/test-pipeline.warhome/sejal/Documents/devops-software/apache-tomcat-9.0.85/webapps'
			}}	
}}
