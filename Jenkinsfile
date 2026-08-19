pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building..."
            }
            post {
                always {
                    emailext (
                        to: "haquynhchi@gmail.com",
                        subject: "Build Status Email",
                        body: "Build was successful!",
                        attachLog: true
                    )
                }
            }
        }
        stage("Test") {
            steps {
                echo "Testing..."
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploying..."
            }
        }
        stage("Complete") {
            steps {
                echo "Completed!"
            }
        }
    }
}