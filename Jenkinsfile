//Declarative
pipeline {
	//agent any
	agent {
		docker {
			image 'maven:3.8.3'
		}
	}
	stages {
		stage('Build'){
			steps {
				sh 'mvn --version'
				echo "Build"
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