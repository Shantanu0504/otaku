pipeline {
	agent any 
	triggers {
  pollSCM '* * * * *'
}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/shantanu/apache-maven-3.9.6-bin/apache-maven-3.9.6/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/otaku.war /home/shantanu/apache-tomcat-9.0.82/webapps'

			}}	
}}

