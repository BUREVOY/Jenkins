pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Ваш шаг сборки проекта
                
                echo "Start of Stage Build"
                echo "Building......."
                bat   "dir App"
                echo "End of Stage Build"
            }
        }
    }
    
    post {
        success {
            // Архивируем артефакты после успешной сборки
            archiveArtifacts artifacts: 'App/**', fingerprint: true
        }
    }
}

