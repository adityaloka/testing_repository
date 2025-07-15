pipeline {
    agent any

    stages {
        stage("Clone Repo") {
            steps {
                echo "This is the clone stage"
                git branch: 'jenkins', url: 'https://github.com/vedantsharmascaler/testing_repo.git' 
            }
        }

        stage("Run Script") {
            steps {
                sh 'chmod +x script.sh'
                sh './script.sh'
            }
        }
    }
}
