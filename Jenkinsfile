pipeline {
    agent {
    //     docker { 
    //         image 'node:20'  // Node.js 20 image from Docker Hub
    //         args '-u root:root' // optional: run as root to avoid permission issues
    //     }
    // }

    environment {
        NODE_ENV = "development"
    }

    stages {
        stage('Checkout') {
            steps {
                echo "🔄 Checking out code from GitHub..."
                git branch: 'main', url: 'https://github.com/ashrith28/nodejs-demo-app.git'
            }
        }

         stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                bat 'docker build -t nodejs-demo-app:latest .'
            }
        }

      stage('Test') {
    steps {
        echo 'Skipping tests (none configured)...'
    }
}


        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                bat '''
                  docker stop nodejs-demo || exit 0
                  docker rm nodejs-demo || exit 0
                  docker run -d -p 3000:3000 --name nodejs-demo nodejs-demo-app:latest
                '''
            }
        }
    }
}
