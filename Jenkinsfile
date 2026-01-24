pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'sudo docker build -t devops-cicd-demo .'
            }
        }

        stage('Deploy Application') {
            steps {
                sh '''
                sudo docker stop devops-cicd-demo || true
                sudo docker rm devops-cicd-demo || true
                sudo docker run -d --name devops-cicd-demo -p 5000:5000 devops-cicd-demo
                '''
            }
        }
    }
}
