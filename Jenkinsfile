pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/alaintruong77/cicd.git'
            }
        }
        stage('Build') {
            steps {
                // Các bước xây dựng dự án của bạn
            }
        }
        stage('Deploy') {
            steps {
                // Giả sử bạn deploy vào /var/www/html (thư mục mặc định của Nginx)
                sh 'cp -r * /var/www/html/'
            }
        }
    }
}
