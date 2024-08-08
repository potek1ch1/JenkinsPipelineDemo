pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello from GitHub hook Trigger'
            }
        }
        stage("Build"){
            steps {
                echo 'Building'
            }
        }
        stage("Deploy"){
            steps {
                echo 'Deploying'
            } 
        }
        stage("Release"){
            steps {
                echo 'Releasing'
            } 
        }
    }
}
