#!groovy
pipeline {
	agent {dockerfile true}
	

	stages {
		stage("Build Docker"){
			steps {
		 	sh 'node --version'
			sh 'svn --version'	
			}
		}
	}
}
