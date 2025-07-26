pipeline {
    agent { label 'test' }

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'test', url: 'https://github.com/gparimaladivya/jenkinsassignment.git'
            }
        }

        stage('Copy to Test Server') {
            steps {
                sh '''
                echo "Copying files to Test Server..."
                mkdir -p ~/testdeploy
                cp -r * ~/testdeploy/
                ls -la ~/testdeploy
                '''
            }
        }
    }
}
