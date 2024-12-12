pipeline {
    agent any
    tools {
        git 'Default' // Sử dụng cài đặt mặc định hoặc tên Git bạn cấu hình
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/alaintruong77/cicd.git'
            }
        }
    }
    stage('Deploy') {
            steps {
                // Giả sử bạn deploy vào /var/www/html (thư mục mặc định của Nginx)
                sh 'cp -r * /var/www/html/'
            }
        }
}