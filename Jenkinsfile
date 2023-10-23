#!/usr/bin/env groovy

pipeline {
    agent none
    stages {
         stage('test') {
            steps {
                script {
                    echo "Testing the application..."
                    echo "Executing pipeline for branch $BRANCH_NAME"
                }
            }
        }
        stage('build') {
            when {
               expression {
                   BRANCH_NAME == "master"
            }
        }
       
        stage('deploy') {
            steps {
                script {
                    echo "Deploying the application..."
                }
            }
        }
    }
}
