pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'My feature branch'
                sh './gradlew build'
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true
        }
    }
}