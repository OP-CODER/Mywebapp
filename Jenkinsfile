pipeline {
    agent any

    tools {
        maven 'Maven 3.9.6' // Match the Maven name configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/OP-CODER/Mywebapp.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy to Tomcat') {
            steps {
                sh 'cp target/MyWebApp.war /C/Tomcat/webapps/'
            }
        }
    }
}
