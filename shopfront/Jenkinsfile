pipeline{
    agent any

    stages{
        stage('Code Checkout'){
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/RohanRusta21/demo-k8s-java-app.git']])
            }
        }
        stage('maven build'){
            steps{
                sh "pwd"
                dir("${env.WORKSPACE}/shopfront"){
                    sh "pwd"
                    sh 'mvn clean package'
                }
            }
        }
    }
}
