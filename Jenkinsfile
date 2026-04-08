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
              echo Stopping old app...
              pm2 delete myapp || echo No app

             echo Starting app with PM2...
               pm2 start app.js --name myapp

             pm2 save

             exit 0
             '''
    }
}
    }
}