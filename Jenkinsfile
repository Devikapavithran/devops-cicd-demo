pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-cicd-demo .'
            }
        }

        stage('Deploy Application') {
            steps {
                sh 'docker rm -f devops-cicd-demo || true'
                sh 'docker run -d -p 5000:5000 --name devops-cicd-demo devops-cicd-demo'
            }
        }
    }
}
