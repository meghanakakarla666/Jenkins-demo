
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Jenkins is checking out the GitHub repository.'
            }
        }

        stage('Check Python') {
            steps {
                bat '"C:\\Users\\Meghana K\\AppData\\Local\\Programs\\Python\\Python37\\python.exe" --version'
            }
        }

        stage('Run Python Tests') {
            steps {
                bat '"C:\\Users\\Meghana K\\AppData\\Local\\Programs\\Python\\Python37\\python.exe" -m unittest -v'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Tests passed. Deployment stage can run.'
            }
        }
    }

    post {
        success {
            echo 'All Python tests passed!'
        }
        failure {
            echo 'Pipeline failed. Check Console Output.'
        }
    }
}
