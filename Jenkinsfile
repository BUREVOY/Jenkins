pipeline {
    agent any

    stages {
        stage('1-Build') {
            steps {
                echo "Start of Stage Build"
                echo "Building......."
                bat   "dir App"
                echo "End of Stage Build"
            }
        }

        post {
            success {
            // Архивируем артефакты после успешной сборки
                archiveArtifacts artifacts: './App/bin/Release/net8.0/publish', fingerprint: true
            }
        }


   }
}