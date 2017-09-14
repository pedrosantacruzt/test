#!groovy
pipeline {
	agent {dockerfile { dir 'configuration' }}
	

	stages {
		stage("Build Docker"){
			steps {
		 	sh 'node --version'
			sh 'svn --version'	
			}
		}
	}
}
