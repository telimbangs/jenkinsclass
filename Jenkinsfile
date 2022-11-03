pipeline {
    agent any
    tools {
        maven "Local Maven"
    }
    environment {

    PATH = "C:\\WINDOWS\\SYSTEM32"

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
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
    }
}
 stage('Test'){
            steps {
                bat 'mvn test'
            }
            post {
             always {
                junit 'target/surefire-reports/*.xml'
            }
        }
    }
}