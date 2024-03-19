pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "first pipeline"
                
            }
        }
        stage('Clone Repository') {
            steps {
                // Клонируем репозиторий Git
                script {
                    git 'clone https://github.com/BUREVOY/Jenkins.git'
                }
            }
        }
        
        stage('List Repository Contents') {
            steps {
                // Выводим содержимое репозитория
                script {
                    sh 'ls -la'
                }
            }
        }

    }
}
