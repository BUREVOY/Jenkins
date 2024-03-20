pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {                
                echo "В начале было слово"
                bat   "dir App"
                dir("${env.WORKSPACE}/App") {
                    bat 'dir'
                        script {
                        // Выполняем сборку Docker образа
                        bat 'docker build -t jenk -f Dockerfile .'
                        bat 'docker run -d jenk'
                    }
                }
                
                echo "congragulations..."
            }
        }
    }
    
    post {
        success {
            // Архивируем артефакты после успешной сборки
            //archiveArtifacts artifacts: 'App/**', fingerprint: true
            // bat 'xcopy /s /y "App\\*" "%WORKSPACE%"'
            bat 'copy /y "App\\bin\\Release\\net8.0\\DotNet.Docker.exe" "%WORKSPACE%"'

        }
    }
}

