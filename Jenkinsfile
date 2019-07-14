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
				sh script: 'docker-compose -f docker-compose.yml up -d --build'
				
			}
		}
	}
}
