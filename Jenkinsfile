pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'develop', url: 'https://github.com/gparimaladivya/jenkinsassignment.git'
            }
        }

        stage('List Files') {
            steps {
                sh 'ls -la'
            }
        }

        stage('Custom Folder') {
            steps {
                sh 'mkdir -p myfolder'
                sh 'cp Jenkinsfile README.md myfolder/'
                sh 'echo "Files copied to myfolder:" && ls -l myfolder'
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: 'myfolder/**', fingerprint: true
        }
    }
}
