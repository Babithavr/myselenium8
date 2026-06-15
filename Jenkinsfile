pipeline {
	agent any
	tools{
		maven 'Maven'
		}
	stages{
		stage('Checkout'){
			steps{
				git branch: 'master',url:'https://github.com/Babithavr/myselenium8.git'
				}
			}
		stage('Build'){
			steps{
				sh 'mvn clean package'
				}
			}
		stage('Test'){
			steps{
				sh 'mvn test'
				}
			}
		stage('Run application'){
			steps{
				sh'nohup java -jar target/myselenium8-1.0-SNAPSHOT.jar'
				}
			}
		}
	post{
		success{
			echo 'success'
			}
		failure{
			echo 'failed'
			}
		}
	}
	
		
