pipeline {
    agent any
    stages{
        stage('Build') {
            steps{
                bat 'maven clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtificats artificats: '**/target/*.war'
                }
            }
        }
        stage('deploy to staging') {
            steps {
                build job: 'deploy-to-staging'
            }
        }
    }
}