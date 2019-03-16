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
                def taskDefile="file://aws/task-definition-${imagetag}.json"
                echo "Building docker Image for BUILD: ${BUILD_NUMBER}"
                echo "${imagetag}"
                echo "${taskDefile}"
                sh ./build_docker_image

            }
        }
    }
}
