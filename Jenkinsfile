pipeline {
    agent any

    stages {
        stage('Check Python') {
            steps {
                bat 'where python'
                bat 'python --version'
                bat 'python -m pip --version'
    }
}


        stage('Clone Repo') {
            steps {
                git 'https://github.com/7afidhou/Jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'python -m pytest tests/'
            }
        }
    }
}
