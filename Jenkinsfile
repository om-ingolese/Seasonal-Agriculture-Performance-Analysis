
pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
                echo 'GitHub code checked out successfully!'
            }
        }

        stage('Verify Project Files') {
            steps {
                bat 'dir'
                echo 'Project files verified successfully!'
            }
        }

        stage('Pipeline Validation') {
            steps {
                echo 'GitHub integration successful!'
                echo 'Pipeline validation completed!'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL!'
        }
        failure {
            echo 'BUILD FAILED! Check Console Output.'
        }
    }
}
