pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000' 
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Development') {
            steps {
                sh 'npm install'
            }
        }
        stage('Staging') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
        stage('Deployment') {
          steps {
            echo 'Hello World'
          }
        }
    }
}
