pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-username/devops-crash-course.git'
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
