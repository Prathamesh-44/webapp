pipeline {
	agent any
	stages {
		stage('Checkout code') {
			steps {
				git branch: 'main',
					url: 'https://github.com/Prathamesh-44/webapp.git'
			}
		}
		stage('Build Docker Image') {
			steps {
        sh 'docker build -t myapp:latest .'
			}
		}
    stage('Stop old container') {
        steps {
            sh '''
              docker stop mycontainer || true
              docker rm mycontainer || true
              docker run -d -p 8081:80 --name mycontainer myapp:latest
            '''
          }
      }
      stage('Verify Container') {
          steps {
              sh 'docker ps'
            }
        }
	}
}
