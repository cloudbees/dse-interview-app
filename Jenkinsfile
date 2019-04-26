pipeline {
    agent any
    tools { 
        maven 'M3'
    }
    options {
        timestamps()
    }
    stages {
        stage('Checkout') {
            steps {
                script {
                    currentBuild.displayName = "Milestone 3: ${BUILD_NUMBER}"
                }
                checkout scm
            }
        }
        stage ('Build and test'){
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
