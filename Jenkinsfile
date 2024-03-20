pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {                
                echo "В начале было слово"
                
                dir("${env.WORKSPACE}/App") {
                    bat 'dir'
                        script {
                        bat 'docker build -t jenk -f Dockerfile .'
                        bat 'docker run jenk'
                    }
                }
                
                echo "congragulations..."
            }
        }
    }
    
    post {
        success {
            bat 'copy /y "App\\bin\\Release\\net8.0\\DotNet.Docker.exe" "%WORKSPACE%"'

        }
    }
}

