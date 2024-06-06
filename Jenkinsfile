pipeline {
    agent any
    stages{
        stage('checkout') {

        git 'https://github.com/rohitlamsonge66/Jenkingsmaven2.git'
        }

         stage('build') {
          bat 'mvn clean compile install test'
          archiveArtifacts artifacts: 'target/*', followSymlinks: false

        }
        stage('Post build') {
        mail bcc: '', body: 'jenkins test mail.', cc: '', from: '', replyTo: '', subject: 'Demo Jenkins Email', to: 'r6831y@gmail.com'
        }
    }
}
