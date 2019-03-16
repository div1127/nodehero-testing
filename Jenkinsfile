pipeline {
    agent {label "ecs-slaves"}

    stages {
        stage('Build') {
            steps {
                echo "Building..."
                sh "npm install"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'npm run test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'docker info'
                sh "apt-get update && apt-get install libltdl-dev -y"
                sh "docker -v"
                sh "aws --version"
                sh "ecs-cli --version"
                
            }
        }
    }
}
