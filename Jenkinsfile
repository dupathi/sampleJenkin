pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                git 'https://github.com/venddy/pipeline.git'
            }
        }
              
           stage('Build') {
            steps {
                bat 'start /b mvn clean install'
            }
        }
        stage('Test') {
            steps {
                bat 'start /b mvn test'
            }
        }
    }
}
