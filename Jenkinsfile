pipeline {
    agent any

    triggers {
        pollSCM('* * * * *') // Check for changes every minute
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'develop', url: 'https://github.com/gparimaladivya/jenkinsassignment.git'
            }
        }

        stage('Run Test Job') {
            agent { label 'test' }
            steps {
                sh '''
                echo "Copying files to Test Node..."
                mkdir -p ~/testdeploy
                cp -r * ~/testdeploy/
                ls -l ~/testdeploy
                '''
            }
        }

        stage('Run Prod Job') {
            agent { label 'prod' }
            steps {
                sh '''
                echo "Copying files to Prod Node..."
                mkdir -p ~/proddeploy
                cp -r * ~/proddeploy/
                ls -l ~/proddeploy
                '''
            }
        }
    }
}
