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
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'java -jar target/myapp.jar'
            }
        }
    }
}
