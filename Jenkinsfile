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
                echo 'Hello Development'
            }
        }
        stage('Staging') {
            steps {
                echo 'Hello Staging'
            }
        }
        stage('Deployment') {
          steps {
            echo 'Hello Deployment'
          }
        }
    }
}
