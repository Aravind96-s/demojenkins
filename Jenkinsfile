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
               taskkill /F /IM node.exe || echo No process

              echo Starting app in separate process...
              start "" cmd /k "cd /d C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\demo && node app.js"

               echo Done
              exit 0
               '''
    }
}
    }
}