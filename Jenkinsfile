pipeline{
	agent any
	tools {
	maven 'Maven'
	}
	stages {
	stage('Checkout'){
	git branch:'master',url:'https://github.com/awsabhi12/abhi00.git'
	}
	stage('Build'){
	sh 'mvn clean package'
	}
	stage('Test'){
	sh 'mvn test'
	}
	
	stage('Run-Application'){
	sh 'java -jar target/abhi00-1.0-SNAPSHOT.jar'
	}
	}
	POST{
		success{
			echo 'build success'
			}
		failure{
			echo 'build failure'
			}
	}
	}
	
	
