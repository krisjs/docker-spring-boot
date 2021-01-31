pipeline {
	agent any
	
	stages{
		stage ('Compile') {
			steps {
				withMaven(maven :'apache-maven-3.6.3'){
					sh 'mvn clean compile'
				}
			}
		
		}
		stage ('Testing') {
		steps {
				withMaven(maven :'apache-maven-3.6.3'){
					sh 'mvn test'
				}
			}
			
		}
		stage ('Deploy') {
		steps {
				withMaven(maven :'apache-maven-3.6.3'){
					sh 'mvn deploy'
				}
			}
			
		}
	}
}