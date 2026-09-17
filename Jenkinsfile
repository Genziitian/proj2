pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                // Replace with your actual GitHub username and repository name
                git branch: 'main', url: 'https://github.com/Genziitian/proj2'
            }
        }
        stage ('Generate Report') {
            steps {
                bat 'python app.py'
            }
        }
        stage ('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
