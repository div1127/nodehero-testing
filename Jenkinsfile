pipeline {
    agent {label "ecs-slaves"}
    def imagetag="repo-${BUILD_NUMBER}"
    

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
                echo "Building docker Image for BUILD: ${BUILD_NUMBER}"
                echo "${imagetag}"
                
                

            }
        }
    }
}
