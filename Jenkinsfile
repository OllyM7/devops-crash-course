pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/OllyM7/devops-crash-course.git' branch: 'main'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install pytest'
                sh 'if [ -f requirements.txt ]; then pip install -r requirements.txt; fi'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest'
            }
        }
    }
}
