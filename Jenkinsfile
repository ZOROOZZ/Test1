pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Deploy to Nginx') {
            steps {
                sh '''
                sudo /bin/cp index.html /var/www/html/index.html
                sudo /bin/systemctl restart nginx
                '''
            }
        }
    }
}
