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
                withCredentials([[
                    $class: 'AmazonWebServicesCredentialsBinding',
                    credentialsId: 'MyAWS',
                    accessKeyVariable: 'AWS_ACCESS_KEY_ID',
                    secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]){
                        sh(script: 'aws s3 cp /var/lib/jenkins/workspace/JenkinsPipeline/index.html s3://test-env-jenkins-potekichi/')
                }
            } 
        }
        stage("Release"){
            steps {
                echo 'Releasing'
            } 
        }
    }
}
