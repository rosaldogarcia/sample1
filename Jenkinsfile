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
		sh "git checkout main"
		sh "git pull origin/main"
		sh "git checkout dev"
		sh "git pull"
		sh "git merge origin/main"
		sh "git push"
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
