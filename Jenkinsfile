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
}
