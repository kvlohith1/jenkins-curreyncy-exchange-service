//Declarative
pipeline {
	agent any
	environment {
		dockerHome = tool "my_docker"
		mavenHome = tool "my_maven"
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build'){
			steps {
				sh 'mvn --version'
				sh 'docker --version'
				echo "PATH - $PATH"
			}
		}
		stage('Test'){
			steps {
				echo "Test"
			}
		}
		stage('Deploy'){
			steps {
				echo "Deploy"
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