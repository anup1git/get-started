pipeline {
    agent any // This tells Jenkins to run the pipeline on any available agent

    tools {
        // This specifies the tools to be automatically installed on the agent
        maven 'Maven_3_6_3' // The name 'Maven_3_6_3' should match the name configured in Jenkins global tool configuration
        jdk 'JDK11' // Make sure the JDK version matches what you've configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                // Checks out the source code from a specified Git repository
                git 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Build') {
            steps {
                // Runs the Maven build command
                script {
                    // This is a basic command to clean the project, compile source code and package it
                    mvn 'clean package'
                }
            }
        }

        stage('Archive Artifacts') {
            steps {
                // Archives the built artifacts
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }

        stage('Deploy') {
            steps {
                // Add deployment steps here
                echo 'Deploying....'
            }
        }
    }
}
