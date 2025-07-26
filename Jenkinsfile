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
                // Create folder if it doesn't exist
                sh 'mkdir -p myfolder'

                // Copy only Jenkinsfile and README.md to myfolder
                sh 'cp Jenkinsfile README.md myfolder/'

                // Show copied files
                sh 'echo "Files copied to myfolder:" && ls -l myfolder'
            }
        }
    }
}
