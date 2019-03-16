#!/bin/groovy
pipeline {
    agent {label "ecs-slaves"}
    environment {
        def imagetag="repo"
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
                echo "Building idocker Image for BUILD: ${BUILD_NUMBER}"
                echo "${imagetag}"
                
                

            }
        }
    }
}
