pipeline {
    agent any

    environment {
        IMAGE_NAME = "ashrith-demo-app"
        CONTAINER_NAME = "jenkins-demo"
    }

    stages {
        stage('Checkout') {
            steps {
                echo "🔄 Checking out code from GitHub..."
                git branch: 'main', url: 'https://github.com/ashrith28/nodejs-demo-app.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Example: run unit tests
                sh 'echo "No tests configured, skipping..."'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Stop and remove old container if exists
                sh '''
                if [ "$(docker ps -aq -f name=$CONTAINER_NAME)" ]; then
                docker stop $CONTAINER_NAME || true
                docker rm $CONTAINER_NAME || true
                fi
                docker run -d -p 3000:3000 --name $CONTAINER_NAME $IMAGE_NAME
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}
