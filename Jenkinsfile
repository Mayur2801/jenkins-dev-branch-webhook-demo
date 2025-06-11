pipeline {
    agent any
    triggers {
        // Poll SCM as fallback every 5 minutes (optional)
        pollSCM('H/5 * * * *')
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
                    userRemoteConfigs: [[url: 'https://github.com/YOUR_GITHUB_USERNAME/jenkins-dev-branch-webhook-demo.git']]
                ]
            }
        }
        stage('Build') {
            steps {
                echo "Running build steps..."
                // Add your build commands here
            }
        }
        stage('Deploy') {
            steps {
                echo "Running deploy steps..."
                // Add your deploy commands here
            }
        }
    }
}

