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
  
        stage ("Build"){
           steps{
              echo "This is the Build Stage"
                 }
           }

        stage ("Test"){
           steps{
              echo "This is the Test Stage"
                 }
           }

        stage ("Deploy"){
           steps{
              echo "This is the Deploy Stage"
                 }
           }
       
     }

}
