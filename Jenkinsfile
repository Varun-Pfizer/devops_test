
pipeline {
    agent any
    environment {
        // Define a variable to store the clone directory based on branch name
        cloneDir = "C:/Users/BHANDV04/OneDrive - Pfizer/Downloads/${env.BRANCH_NAME}"
    }
    stages {
        stage('Clone Github Project') {
            steps {
                script {
                    dir("${env.cloneDir}") { // Use the dynamic environment variable
                        git branch: ${env.BRANCH_NAME},
                           credentialsId: 'id1',
                           url: 'https://github.com/Varun-Pfizer/devops_test.git'
                    }
                }
            }
        }
    }
}
