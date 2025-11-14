

pipeline {
	//agent any
	agent { 
		docker {
			image 'maven:3.8.1-jdk-11' 
		}
	}
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	}
	post {
		always {
			echo "I'm awesome! I will always run!"
		}
		success {
			echo "I run when you are successful!"
		}
		failure {
			echo "I run when you fail!"
		}
	}
}
