pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Клонируем репозиторий
                    git 'https://github.com/ваш_репозиторий.git'

                    // Выполняем сборку
                    sh 'node index.js'
                }
            }
        }
    }
}
