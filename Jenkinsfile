pipeline {
    agent any
    environment {
        //be sure to replace "bhavukm" with your own Docker Hub username
        DOCKER_IMAGE_NAME = "bhavukm/train-schedule"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
        stage('Build Docker Image') {
            when {
                branch 'master'
            }
            steps {
                script {
                    app = docker.build(DOCKER_IMAGE_NAME)
                    app.inside {
                        sh 'echo Hello, World!'
                    }
                }
            }
        }
        stage('Push Docker Image') {
            when {
                branch 'master'
            }
            steps {
                echo 'Running build automation'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                
                
            }
        }
        stage('CanaryDeploy') {
            when {
                branch 'master'
            }
            steps {
                echo 'CanaryDeploy Successfull'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                
            }
        }
        stage('DeployToProduction') {
            when {
                branch 'master'
            }
           
            steps {
                echo 'DeployToProduction Successfull'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                 echo 'Running build automation'
                sh './gradlew build --no-daemon'
                 echo 'Running build automation'
                sh './gradlew build --no-daemon'
                 echo 'Running build automation'
                sh './gradlew build --no-daemon'
                 echo 'Running build automation'
                sh './gradlew build --no-daemon'
                 echo 'Running build automation'
                sh './gradlew build --no-daemon'
                
            }
         
        }
    }
}
