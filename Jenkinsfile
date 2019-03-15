pipeline {
    agent {label "ecs-slave"}

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
