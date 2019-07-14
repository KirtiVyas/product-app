pipeline {
    agent any


    stages {
        stage('SCM Checkout'){
          git 'https://github.com/KirtiVyas/product-app.git'
        }
    }
    {
		stage('trigger the docker-compose') {
			steps {
				sh label: '', script: 'docker-compose -f /var/jenkins_home/workspace/newpipelinejob1/docker-compose.yml up -d --build'
				
			}
		}
	}
}
