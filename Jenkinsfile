pipeline {
	agent any
	stages {
		stage('Clone repository') {
			steps {
				git branch: 'main',
					url: 'https://github.com/Prathamesh-44/webapp.git'
			}
		}
		stage('Build Message') {
			steps {
				echo 'Github repository cloned successfully!'
				echo 'Jenkins pipeline executed successfully!'
			}
		}
	}
}
