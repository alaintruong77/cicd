pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/<username>/static-website.git'
            }
        }
        stage('Deploy Website') {
            steps {
                sh '''
                docker rm -f static-website || true
                docker run -d --name static-website -p 80:80 \
                -v $(pwd):/usr/share/nginx/html nginx
                '''
            }
        }
    }
}
