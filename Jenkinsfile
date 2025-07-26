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
                sh '''
                    mkdir -p myfolder
                    cp Jenkinsfile README.md myfolder/
                    echo "Files copied to myfolder:"
                    ls -l myfolder
                '''
            }
        }
    }
}
