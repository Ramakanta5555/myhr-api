pipelione{
    agent any

    stages{
        stage("git checkout"){
            steps{
                git url:"https://github.com/Ramakanta5555/myhr-api"
            }
        }
        stage("Maven Build"){
            steps{
                sh "mvn clean package"
            }
        }
        stage("Dev Deploy"){
            steps{
                echo "Deploying to Dev"
            }
        }

    }
}