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
        stage('Codecoverage') {
            steps {
                echo 'Codecoverage'
                
            }
        }
    }
}
