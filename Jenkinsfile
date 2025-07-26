pipeline {
    agent { label 'prod' }

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'master', url: 'https://github.com/gparimaladivya/jenkinsassignment.git'
            }
        }

        stage('Copy to Prod Server') {
            steps {
                sh '''
                echo "Copying files to Prod Server..."
                mkdir -p ~/proddeploy
                cp -r * ~/proddeploy/
                ls -la ~/proddeploy
                '''
            }
        }
    }
}
