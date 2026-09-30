pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'GitHub repository is connected!'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage is running!'
            }
        }

        stage('Success') {
            steps {
                echo 'Jenkins Pipeline completed!'
            }
        }
    }
    post {
    success {
        emailext(
            subject: "Jenkins Build Successful",
            body: "Your Jenkins pipeline completed successfully.",
            to: "itsmerishithareddyk@gmail.com"
        )
    }
    failure {
        emailext(
            subject: "Jenkins Build Failed",
            body: "Your Jenkins pipeline failed. Please check the console output.",
            to: "itsmerishithareddyk@gmail.com"
        )
    }
}
}
// Testing GitHub webhook integration
