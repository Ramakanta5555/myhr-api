pipeline{
    agent any

    stages{
        stage("git checkout"){
            steps{
                git url:"https://github.com/Ramakanta5555/myhr-api", branch: "main"
            }
        }
        stage("Maven Build"){
            steps{
                sh "mvn clean package"
            }
        }
        stage("Dev Deploy"){
            when{
                branch 'develop'
            }
            steps{
                echo "Deploying to Dev"
            }
        }
        stage("QA Deploy"){
            when{
                branch 'qa'
            }
            steps{
                echo "Deploying to qa"
            }
        }
    }
}