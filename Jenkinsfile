pipeline {
    agent any // This tells Jenkins to run the pipeline on any available agent

    tools {
        // This specifies the tools to be automatically installed on the agent
        maven 'Maven_3_9_9' // The name 'Maven_3_6_3' should match the name configured in Jenkins global tool configuration
        jdk 'JDK17' // Make sure the JDK version matches what you've configured in Jenkins
    }

    stages {
       
        stage('Build') {
            steps {
                // Runs the Maven build command
                script {
                    // This is a basic command to clean the project, compile source code and package it
                    cd micro-services/employee-service
                    sh '/usr/lib/maven/3/apache-maven-3.9.9/bin/mvn clean package'
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
