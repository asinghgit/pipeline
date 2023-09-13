pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            //    sh 'echo hello world'
            }
		}
        stage('Checkout'){
            steps {
                checkout([$class: 'GitSCM', 
			  branches: [[name: 'main']], 
			  extensions: [], 
			  userRemoteConfigs: [[credentialsId: 'newPipelineI',
			  url: 'https://github.com/asinghgit/hackathon.git']]])
				}
		}
		stage('bulid the code'){
			steps {
				bat 'mvn clean install'
				bat 'echo Hi 123' 
			}
		}
	}
}
