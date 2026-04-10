pipeline {
    agent any

    tools {
        maven 'Maven3'  // Maven installation name in Jenkins
        jdk 'Java21'    // JDK installation name in Jenkins
    }

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }
    }

    post {
        always {
            echo "Pipeline finished!"
        }
    }
}
