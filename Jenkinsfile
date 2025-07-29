pipeline {
    agent any

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
