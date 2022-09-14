//Declarative
pipeline {
	agent any
	stages {
		stage('Build'){
			steps {
				echo "BUILD NUMBER - $env.BUILD_NUMBER"
				echo "BUILD ID - $env.BUILD_ID"
				echo "Job Name - $env.JOB_NAME"
				echo "BUILD URL - $env.BUILD_URL"
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