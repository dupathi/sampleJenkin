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
                bat 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}
