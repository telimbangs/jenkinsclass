pipeline {
    agent any
    tools {
        maven 'Local Maven'
    }
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/telimbangs/jenkinsclass.git',
                    credentialsId: 'TT',
                    branch 'jenkinsmain'
            }
        }
    }
}

