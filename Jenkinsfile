pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo "Building the code using Maven to compile and package the application into a deployable artefact (.jar/.war)"
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo "Running unit tests using JUnit to check individual code components"
                echo "Running integration tests using Postman to check that different components work together as expected"
            }
        }

        stage('Code Analysis') {
            steps {
                echo "Analysing the code using SonarQube to check that it meets industry coding standards and to detect code smells"
            }
        }

        stage('Security Scan') {
            steps {
                echo "Scanning the code and its dependencies using Snyk to identify known vulnerabilities"
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo "Deploying the application to a staging server (AWS EC2 instance) using the AWS CLI"
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo "Running integration tests on the staging environment using Selenium to confirm the application behaves correctly in a production-like setting"
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying the application to the production server (AWS EC2 instance) using the AWS CLI"
            }
        }
    }
}
//This to check if edits appear//
