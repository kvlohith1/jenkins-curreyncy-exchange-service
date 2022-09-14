//Declarative
pipeline {
	agent any
	environment {
		dockerHome = tool "my_docker"
		mavenHome = tool "my_maven"
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Checkout') {
			steps {
				sh 'mvn --version'
				sh 'docker --version'
				echo "PATH - $PATH"
			}
		}
		stage('Compile') {
			steps {
				sh 'mvn clean compile'

			}
		}
		stage('Test') {
			steps {
				sh 'mvn test'
			}
		}
		stage('Integration Test') {
			steps {
				sh 'mvn failsafe:integration-test failsafe:verify'
			}
		}
	}
	post {
		always {
			echo 'I run always'
		}
		success {
			echo "i am successful."
		}
		failure {
			echo 'I failed'
		}
	}
}