pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Spygram/demo1-webapp.git'
            }
        }

        stage('Build') {
            steps {
                withMaven(maven:'maven'){
                    sh 'mvn clean package'
                }
            }
        }
        stage('deploy'){
            steps{
                deploy adapters: [tomcat8(credentialsId: 'tomcat_deployer', path: '', url: 'http://172.31.24.113:8080')], contextPath: null, war: '**/*.war'
            }
        }
    }
}