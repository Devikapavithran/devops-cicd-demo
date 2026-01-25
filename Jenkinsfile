pipeline {
    agent any

    environment {
        IMAGE_NAME = "devikapavithran/devops-cicd-demo"
        DOCKER_CREDS = "dockerhub-creds"
    }

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devikapavithran/devops-cicd-demo:latest .'
            }
        }

        stage('Push Image to Docker Hub') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-creds',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {
                    sh '''
                    echo "$DOCKER_PASS" | docker login -u "$DOCKER_USER" --password-stdin
                    docker push devikapavithran/devops-cicd-demo:latest
                    '''
                }
            }
        }

        stage('Deploy Application') {
            steps {
                sh '''
                docker rm -f devops-cicd-demo || true
                docker pull devikapavithran/devops-cicd-demo:latest
                docker run -d -p 5000:5000 --name devops-cicd-demo devikapavithran/devops-cicd-demo:latest
                '''
            }
        }
    }
}
