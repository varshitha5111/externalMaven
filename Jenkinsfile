pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('CheckOut'){
			step{
				git branch:'master', url : 'https://github.com/varshitha5111/externalMaven.git'
			}
		}
		stage('Build'){
			step{
				sh 'mvn clean install'
			}
		}
		stage('Test'){
			step{
				sh 'mvn test'
			}
		}
		stage('Run Application'){
			step{
				sh 'java - jar target/MyMavenApp-1.0-SNAPSHOT.jar'
			}
		}
	}
}
