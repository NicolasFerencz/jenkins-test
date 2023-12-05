/* Requires the Docker Pipeline plugin */
pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'npm run start'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
            slackSend(color: 'blue', message: 'hello', channel: "#fc-jenkins-test")
        }
    }
}