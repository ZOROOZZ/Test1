pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Deploy to Nginx') {
            steps {
                sh '''
                sudo cp index.html /var/www/html/index.html
                sudo systemctl restart nginx
                '''
            }
        }
    }
}
