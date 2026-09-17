pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                // Pulls code from your repository
                git branch: 'main', url: 'https://github.com/mahe-vit/project2_ass07.git'
            }
        }
        stage ('Generate Report') {
            steps {
                // Executes your python script on Windows environment
                bat 'python app.py'
            }
        }
        stage ('Archive Report') {
            steps {
                // Keeps a downloadable copy of report.txt in Jenkins UI
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
