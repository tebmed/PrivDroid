pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/tebmed/PrivDroid'
            }
        }
        stage('Build Plugin') {
            steps {
                sh './gradlew buildPlugin'
            }
        }
        stage('Run Tests') {
            steps {
                sh './gradlew test'
            }
        }
    }
}
