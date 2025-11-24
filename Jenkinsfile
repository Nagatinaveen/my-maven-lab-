pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
                echo "Latest commit:"
                sh 'git log -1 --oneline'
                echo "Changed files:"
                sh 'git log -1 --name-only'
            }
        }

        stage('Webhook Test') {
            steps {
                echo "Webhook Triggered Successfully!"
            }
        }
    }
}
