pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh 'echo hello world'
                checkout([$class: 'GitSCM', branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[credentialsId: 'newPipelineI', url: 'https://github.com/asinghgit/hackathon.git']]])
            }
        }
    }
}
