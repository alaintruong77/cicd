pipeline {
    agent any
    tools {
        git 'Git' // Sử dụng Git tool đã cấu hình
    }
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/alaintruong77/cicd.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh '''
                docker build -t static-website-image .
                '''
            }
        }
        stage('Deploy Website') {
            steps {
                sh '''
                docker rm -f static-website || true
                docker run -d --name static-website -p 80:80 \
                -v $(pwd)/public:/usr/share/nginx/html \
                static-website-image
                '''
            }
        }
        stage('Cleanup') {
           steps {
                sh '''
                    docker system prune -af
                '''
           }
        }
    }
}