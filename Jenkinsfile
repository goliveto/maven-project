pipeline {
    agent any
    tools {
        maven 'maven-3.6.0'
        jdk 'JAVA_8'
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
                bat "docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        }
    }
}