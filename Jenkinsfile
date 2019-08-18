pipeline {
    agent any
    tools {
        maven 'maven-3.6.0'
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
    }
}