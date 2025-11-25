pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/ZOROOZZ/Test1.git'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh '''
                sudo cp index.html /var/www/html/index.html
                sudo systemctl restart nginx
                '''
            }
        }
    }

    post {
        success {
            echo "Website updated successfully after GitHub push!"
        }
    }
}
