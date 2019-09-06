pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3005:3005' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Test'){
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
