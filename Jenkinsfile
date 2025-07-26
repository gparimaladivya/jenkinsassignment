pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'develop', url: 'https://github.com/gparimaladivya/jenkinsassignment.git'
            }
        }

        stage('Run Test Job') {
            steps {
                build job: 'Push-to-Test'
            }
        }

        stage('Run Prod Job') {
            steps {
                build job: 'Push-to-Prod'
            }
        }
    }
}
