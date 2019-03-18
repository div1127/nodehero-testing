#!/bin/groovy
pipeline {
    agent {label "ecs-slaves"}
    environment {
        def imagetag="nodejs-repo-${BUILD_NUMBER}"
        def taskDefile="file://aws/task-definition-${imagetag}.json"
    }

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
                sh "docker build -t ${imagetag} ."
                
                

            }
        }
    }
}
