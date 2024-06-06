pipeline {
    agent any
    stages{
        stage('checkout') {
            steps{
                echo 'Checking out !!'
                git 'https://github.com/rohitlamsonge66/Jenkingsmaven2.git'
            }
        }

         stage('build') {

            steps{
                 echo 'build and archive out !!'
                           bat 'mvn clean compile install test'
                           archiveArtifacts artifacts: 'target/*', followSymlinks: false
                 }
        }
        stage('Post build') {
        steps{
              echo 'Send mail !!'
              mail bcc: '', body: 'jenkins test mail.', cc: '', from: '', replyTo: '', subject: 'Demo Jenkins Email', to: 'r6831y@gmail.com'

             }
        }
    }
}
