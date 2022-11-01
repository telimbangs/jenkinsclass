pipeline {
    agent any
    tools {
        maven "Local Maven"
    }
    stages {
        stage('Checkout') {
            steps {
                // Get some code from a GitHub repository
                git url: 'https://github.com/telimbangs/jenkinsclass.git', 
                    branch: 'jenkinsmain',
                    credentialsId: 'TT'
            }
        }
    }
}