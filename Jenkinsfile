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
        stage('Docker Build & Push') {
            steps {
                def imagetag="nodejs-app-${BUILD_NUMBER}"
                
                echo "Building docker Image for BUILD: ${BUILD_NUMBER}"
                echo "${imagetag}"
                
                

            }
        }
    }
}
