pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
    }

    post {
        success {
            emailext (
                subject: "Jenkins Job Successful: ${env.JOB_NAME}",
                body: """The job ${env.JOB_NAME} (#${env.BUILD_NUMBER}) has completed successfully.
Check it here: ${env.BUILD_URL}""",
                to: 'adityalokapalli309@gmail.com'
            )
        }

        failure {
            emailext (
                subject: "Jenkins Job Failed: ${env.JOB_NAME}",
                body: """The job ${env.JOB_NAME} (#${env.BUILD_NUMBER}) has failed.
Check logs: ${env.BUILD_URL}""",
                to: 'adityalokapalli309@gmail.com'
            )
        }
    }
}
