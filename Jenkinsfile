pipeline {
    agent any

    stages {
        stage('1-Build') {
            steps {
                echo "Start of Stage Build"
                echo "Building......."
                bat   "dir App"
                bat   "echo hello > file.txt"
                echo "End of Stage Build"
            }
        }

   }
}