pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build') {
            steps {
                echo "Build successful"
            }
        }

        stage('Deploy') {
            steps {
              bat '''
              echo Killing old node process...
              taskkill /F /IM node.exe >nul 2>&1 || echo No process

              echo Starting app...
              cd /d C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\demo
              start /B node app.js

              echo Done
               '''
    }
}
    }
}