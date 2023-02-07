pipeline {
    agent any

    stages {
	stage ('Checkout sample1 project') {
 	    steps {
	   	git branch: 'main',
	 	credentialsId: 'rosaldogarcia',
		url: 'git@github.com:rosaldogarcia/sample1.git'
		sh "ls -ltr" 
	   }
	}
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
