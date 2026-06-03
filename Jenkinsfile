pipeline {
    agent any

    environment {
        AWS_REGION = 'ap-south-1'
        ECR_REPO = '713520983527.dkr.ecr.ap-south-1.amazonaws.com/shopsphere-app'
        IMAGE_TAG = "v${BUILD_NUMBER}"
    }

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/prajwalahirrao/shopsphere-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t shopsphere-app:${IMAGE_TAG} .'
            }
        }

        stage('Login to ECR') {
            steps {
                sh '''
                aws ecr get-login-password --region $AWS_REGION | \
                docker login --username AWS --password-stdin $(echo $ECR_REPO | cut -d'/' -f1)
                '''
            }
        }

        stage('Tag Docker Image') {
            steps {
                sh 'docker tag shopsphere-app:${IMAGE_TAG} $ECR_REPO:${IMAGE_TAG}'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push $ECR_REPO:${IMAGE_TAG}'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh '''
                kubectl set image deployment/shopsphere-deployment \
                shopsphere-container=$ECR_REPO:${IMAGE_TAG}
                '''
            }
        }

        stage('Verify Rollout') {
            steps {
                sh 'kubectl rollout status deployment/shopsphere-deployment'
            }
        }
    }
}
