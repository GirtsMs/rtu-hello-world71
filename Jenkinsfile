pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Building micro-service.'
            }
        }
        stage('deploy-dev') {
            steps {
                deploy("DEV")
            }
        }
        stage('test-dev') {
            steps {
                running("DEV")
            }
        }
        stage('deploy-stg') {
            steps {
                deploy("STG")
            }
        }
        stage('test-stg') {
            steps {
                running("STG")
            }
        }
        stage('deploy-prd') {
            steps {
                deploy("PRD")
            }
        }
        stage('test-prd') {
            steps {
                running("PRD")
            }
        }
    }
}

def deploy(String environment){
    echo "Deploying micro-service to ${environment} environment."
}

def running(String environment){
    echo "Running tests on ${environment} against micro-service."
}