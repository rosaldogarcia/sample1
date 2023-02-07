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
        stage('Checkout sample-merge project') {
            steps {
		git branch: 'main',
		credentialsId: 'rosaldogarcia',
		url: 'git@github.com:rosaldogarcia/sample-merge.git'  
                sh "ls -ltr"
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
