pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Aravind96-s/demojenkins.git'
            }
        }

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

                echo Starting app in background...
                start "" cmd /c "node app.js"
               '''
    }
}
    }
}