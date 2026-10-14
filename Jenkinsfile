
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
                bat 'if not exist "Seasonal_Agriculture_Performance_Analysis.ipynb" exit /b 1'
                bat 'if not exist "agriculture_dataset.csv" exit /b 1'
                echo 'Notebook and dataset found!'
            }
        }

        
stage('Pipeline Validation') {
    steps {
        echo 'GitHub checkout completed successfully!'
        echo 'Project files verified successfully!'
        echo 'Pipeline validation completed!'
    }
}

    }

    post {
        success {
            echo 'BUILD SUCCESSFUL!'
        }
        failure {
            echo 'BUILD FAILED! Check the Console Output.'
        }
    }
}
