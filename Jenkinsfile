pipeline {
    agent any
    triggers {
        pollSCM('H/5 * * * *')  // Poll every 5 minutes as fallback
    }
    stages {
        stage('Checkout') {
            when {
                branch 'development'
            }
            steps {
                echo "Checking out development branch"
                checkout scm: [
                    $class: 'GitSCM', 
                    branches: [[name: 'refs/heads/development']], 
                    userRemoteConfigs: [[url: 'https://github.com/Mayur2801/jenkins-dev-branch-webhook-demo.git']]
                ]
            }
        }
        stage('Build') {
            steps {
                echo "Running build steps..."
            }
        }
        stage('Deploy') {
            steps {
                echo "Running deploy steps..."
            }
        }
    }
}
