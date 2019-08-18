pipeline {
    agent any
    tools {
        maven 'maven-3.6.0'
        java 'JAVA_8'
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
    }
}