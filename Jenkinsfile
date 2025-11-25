pipeline {
    agent any

    tools {
        maven 'MAVEN-HOME'    // Use the actual Maven install name
        jdk 'JDK17'           // Use the actual JDK install name
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy stage (customize as needed)'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESS'
        }
        failure {
            echo 'BUILD FAILURE'
        }
    }
}
