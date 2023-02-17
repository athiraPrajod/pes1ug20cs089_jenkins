pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				sh 'g++ -o task5 task5.cpp'
				echo 'Build stage successful'
			}
		}
		
		stage('Test') {
			steps {
				sh './task5'
				echo 'Test stage successful'
				post {
					always {
						junit 'target/surefire-reports/*.xml'
					}
				}
			}
		}
		stage('Deploy') {
			steps {
				echo 'Deployment successful'
			}
		}
	}
	
	post {
		failure {
			echo 'Pipeline failed'
		}
	}
}

