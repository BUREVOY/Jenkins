pipeline {
    agent any

    stages {
        stage('1-Build') {
            steps {
                echo "Start of Stage Build"
                echo "Building......."
                bat   "dir App"
                bat   "@echo off"
                bat   "echo hello > example.txt"
                echo "End of Stage Build"
            }
        }

   }
}