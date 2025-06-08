pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('CheckOut'){
			steps{
				git branch:'master', url : 'https://github.com/varshitha5111/externalMaven.git'
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean install'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('Run Application'){
			steps{
				sh 'java - jar target/MyMavenApp-1.0-SNAPSHOT.jar'
			}
		}
	}
}
